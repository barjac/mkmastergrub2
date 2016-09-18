# mkmastergrub2
A bash script to create a master grub2 menu for multi-booting systems.
This script creates a basic Master grub2 install to chainload
into any systems on a machine.
It is intended to be used from a Mageia UEFI installation >= Mageia 5.
Further menu entries may be added manually to master-grub's
custom.cfg at any time which will not be overwritten if the script is
re-run to automatically pick up any new systems added to a machine.
A small (20MB) ext2 (native linux) partition labelled "master-grub"
must be prepared and formatted before running this script.
Run as root:
  # ./mkmastergrub2
