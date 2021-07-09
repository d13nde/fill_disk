# fill_disk
bash script to fill a disk to see, if transfer rates drop or disk is completely writeable.
This is done by generating directories and files, which get filled by random data.
Therefore the disk needs to have a filesystem.

CAUTION: Don't use this on flash media like SSDs or USB-Sticks, since this REALLY writes a lot and weares the drive!

Hacked this together for my personal needs as a bash script.
Dropped it here in case someone else might find it useful.

Requirements to run this script:
- bash
- dd
- openssl
As far as I know, these are all pretty standard on \*nix systems.

usage: fill_disk [-d dircount] [-f filecount] [-b maxblockcount] [-s blocksize] [-v] [-q] [-h]

help:
fill_disk - Fill Disk with random data for testing
  options:
    -d <num> : set max number of dirs to create
    -f <num> : set max number of files to create
    -b <num> : set max count of blocks per file (gets multiplied by 1024)
    -s <str> : set dd blocksize like 4M for 4 MBytes
    -v       : set verbose mode
    -q       : set quiet mode (writes all output to logfile)
    -h       : give this help

  defaults: fill_disk -d 50 -f 50 -b 8 -s 1M
