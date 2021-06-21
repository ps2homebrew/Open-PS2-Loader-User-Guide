**HDD mode**
============

-  **Note :** HDD USB users must of course refer to this
   :ref: `page <usb_mode>`.

| Open PS2 Loader 0.9.3 supports internal HDD, up to 2TB (limit). Your
  HDD can be either an IDE HDD connected directly to the Network Adapter
  or a SATA HDD connected to the Network Adapter using an IDE-to-SATA
  adapter. Non-SONY HDD are supported. You can check an (old) HDD
  compatibility list `here <http://ps2drives.x-pec.com/?p=list>`__.
  Network Adapter clones are not recommended – their quality may vary,
  some may work, some don’t… Well, get away from them and pick a genuine
  SONY one.
| Your HDD requires to be formatted to PSF (SONY own formatting scheme
  and filesystem) before you can install any games on it. Your games
  must be installed in the HDLoader format – you can not installed them
  as .iso.

.. image:: 3629385419-hdd.png
   :alt: title

*Formatting your internal HDD :*
--------------------------------

The recommended method to format your internal HDD to PSF is
`uLaunchELF <http://psx-scene.com/forums/f113/unofficial-launchelf-v4-42-a-37242/>`__.
[FileBroswer > MISC > HddManager > R1 > Format]. Using WnHiip to format
your PS2 HDD is not recommended.

----

*Installing PS2 games :*
------------------------

Before you can install your PS2 games on your internal HDD, you need to
make a image of them – using your favorite dump software (you can use
`ImgBurn <http://imgburn.com/>`__ for that).

OPL supports HDLoader format for internal HDD. They are several ways and
tools to install games on your internal HDD :

-  **using the CD/DVD drive :**

| 
| .
  `HDLGameInstaller <http://ichiba.geocities.jp/ysai187/PS2/HDLGameInstaller.htm>`__
  – by SP193 (PSX-scene thread
  `here <http://psx-scene.com/forums/f19/hdlgameinstaller-v0-807-obt-115321/>`__).
| Please note that DVD9 games can’t be installed this way (CD/DVD drive
  limitation).

-  **over the network, using a pc client :**

| 
| . OPL embedded :ref:`HDL server <hdl_server>`
| .
  `HDLGameInstaller <http://ichiba.geocities.jp/ysai187/PS2/HDLGameInstaller.htm>`__
  – by SP193.
| . `HDL_Dump <https://bitbucket.org/AKuHAK/hdl-dump>`__ – by AKuHAK
  (PSX-scene thread
  `here <http://psx-scene.com/forums/f19/new-reworked-hdl_dump-0-9-1-attempt-gain-full-access-hdd-over-network-113411/>`__).

-  **your HDD directly connected to your PC :**

| 
| . `HDL_Dump <https://bitbucket.org/AKuHAK/hdl-dump>`__ – by AKuHAK
  (PSX-scene thread
  `here <http://psx-scene.com/forums/f19/new-reworked-hdl_dump-0-9-1-attempt-gain-full-access-hdd-over-network-113411/>`__).
| . `WinHIIP 1.7.6 <http://sksapps.com/winhiip_tutorial.html>`__

----

*OPL HDD mode :*
----------------

You need to enable your internal HDD before you can use it. In OPL menu,
go to Settings and set HDD device start mode to MANUAL or AUTO. You
should now be able to access the HDD Games page. If you have enabled the
device and if your PS2 games aren’t displayed in the HDD games page,
there are a few possible things to check :

-  your HDD has not been formatted to the PS2Format for HDL compliant
   partitioning ;
-  games were not installed properly (errors, bad sectors,wrong
   program,etc) ;
-  your network adapter is not working / bad connection ;
-  you are using a network adapter clone ;
-  the HDD is not compatible or damaged/defective ;
-  (...)

**Note :** OPL has now error codes that help you to troubleshoot your
HDD setup.

**Error code > what to do :**

-  %d: HardDisk Drive not detected >
-  %d: HardDisk Drive not formatted >
-  %d: No network adaptor detected >
