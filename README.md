# mkmastergrub2
A bash script to create a master grub2 menu for multi-booting systems.
This script creates a basic Master grub2 instalation to chainload
into any systems on a machine.

It is intended to be used from a Mageia UEFI installation >= Mageia 5.

Further menu entries may be added manually to master-grub's
custom.cfg at any time which will not be overwritten if the script is
re-run to automatically pick up any new systems added to a machine.

A small (20MB) ext2 (native linux) partition labelled "master-grub"
must be prepared and formatted before running this script.

Run as root:
 ./mkmastergrub2
 
To prevent future updates to Mageia from changing the UEFI boot order
in nvram, go to:

Mageia Control Centre -> Boot -> Set Up Boot System.

Progress through the screens until the screen with the option 
to 'Probe Foreign OS', with an Advanced button below.

Go into Advanced and check the box labelled:

"Do not touch ESP or MBR".

Click OK and ignore the warnings about not having a bootloader
installed, on the way to the Finish button.

Any other systems installed on the same hardware should also be 
configured to not disturb the nvram (where uefi boot order is stored).

