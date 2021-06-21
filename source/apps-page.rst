**Apps Page**
=============

Open PS2 Loader 0.9.3 features an ELF loader, that can launch apps
directly from a list – much the same as you would for PS2 games – from
any device. You will need to manually create a configuration file named
**conf_apps.cfg** (lowercase).

conf_apps.cfg file will be read / loaded / saved in this order
(basically from the faster to the slowler device) :

**MC0 >> MC1 >> HDD >> USB**

If OPL fails to write or find conf_apps.cfg on MC, it looks on HDD and
etc…

For HDD, conf_apps.cfg is stored in the root of the +OPL partition ; for
USB, it is stored in the root of the USB device.

*Create the conf file :*
------------------------

Open any text editor , create a new document and make an entry for each
app you wish displayed in OPL. This file will go in
mc?:/OPL/conf_apps.cfg. You can also use uLaunchELF to create this file
from the PS2. [FileBrowser > MISC > TextEditor]

Syntax :

::

   Name of app=Path to file

Example:

::

   uLaunchELF=mc?:/BOOT/BOOT.ELF

-  “Name of app” will be the Title Name displayed in the list.
-  “Path to file” will be where your apps are stored, be sure to use a
   device you plan to have enabled or it will not launch if the device
   is not enabled.

----

*Paths for each device :*
-------------------------

-  for **memory card** : you can launch ELFs from either MC. You can
   either specify on which MC your ELF is stored on (mc0:/ for MC in
   slot1 and mc1:/ MC in slot2) or use mc?:/ for OPL to look on both MCs
   for the file.

Examples:

::

   Sega Master System Emulator=mc0:/APPS/SMSE.ELF
   Sega Mega Drive Emulator=mc1:/BOOT/PGEN.ELF
   PlayStation Emulator=mc?:/BETA/PS2PSXe.ELF

-  for **usb device** : you can launch ELFs from either of the USB
   Slots. ELF files can be on the root or in a subfolder. Simply use the
   mass: prefix, or if you have more than one USB device connected
   mass0:/, mass1:/, etc.

Examples :

::

   Sega Master System Emulator=mass:/ELFS/SMSE.ELF
   Sega Mega Drive Emulator=mass0:/PGEN.ELF

-  for **smb share** : ELF files can be on the root or in a subfolder.
   Use the smb:/ prefix, or smb0:/

Examples :

::

   CodeBreaker v10=smb:/BOOT/CBv10 BOOT noCdStop.ELF
   GSM=smb0:/BOOT/GSM.ELF
   Simple Media System=smb:/SMS.ELF
   uLaunchELF=smb0:/BOOT.ELF

-  for **HDD** : ELFs on HDD must be put in the “+OPL” Partition. The
   “hdd0:+OPL” partition is mounted by OPL into a “virtual” device
   called pfs0:/. You must use this prefix for your path.

Examples :

::

   Sega Mega Drive Emulator=pfs0:/APPS/PGEN.ELF

----

*Launching the apps :*
----------------------

| You will need to enable “Applications start mode” (AUTO or MANUAL) in
  the Settings screen before you can access apps page and launch any
  apps.
| Simply select an app to launch and press the select button to launch
  it.

**Notes :**

-  Some apps can just not be launched from a certain device ;
-  Some apps can just not be launched from OPL page ;
-  Some apps can just not be launched from the last OPL stable version.

**Note :** if you got the “Error : cannot run the item” message when
trying to run an app, check the path in conf_apps.cfg.
