# fill_disk
bash script to fill a disk to see, if transfer rates drop or disk is completely writeable.
This is done by generating directories and files, which get filled by random data.
Therefore the disk needs to have a filesystem.

CAUTION: Don't use this on flash media like SSDs or USB-Sticks, since this REALLY writes a lot and weares the drive!
