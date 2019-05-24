# Enter shell from grub

1. In grub menu, enter "e".
2. Find the kernel line and add either single or init=/bin/sh to the end of it then press Ctrl + X to boot.

The remount the system partition with R/W permission: `mount -o remount rw /`
