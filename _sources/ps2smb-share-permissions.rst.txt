.. _ps2smb_share_permissions:

**How to share PS2SMB folder over the network and set permissions for access**
==============================================================================

*Windows XP :*
--------------

**Enable file sharing :**

Simple File Sharing is on by default , so most likely you have SMB
enabled, but if you don’t or don’t wish to enable it, you can enable the
Guest Account to connect to the SMB share.

| 1. Ensure that Simple File Sharing is enabled (it should be on by
  default). To check do this : [My computer > Tools > Folder Options >
  View tab]. Scroll down in the window and make sure that “Use Simple
  File Sharing (Recommended)” is ticked. Press OK.
| Note : WinXP Home doesn’t have this option as it is ON by default and
  can not be turned OFF.

**Setting a Sharename :**

2. Right click on the folder you want to share (or Partition drive), and
go to “Sharing and Security” (sharing a drive will prompt a warning
first about the risks of sharing it over a network).

3. In Network Sharing and Security, place a mark in the box for “Share
this folder on the network”, then give the “Share Name” the name PS2SMB
(default name) – or any name you want, but it must match into OPL
network configuration. Place also a mark in the box for “Allow network
users to change my files”.

.. image:: 2853784650-xp_share.png
   :alt: title

| **Sources :**
| . `OPL 0.8 User
  Guide <http://opl.sksapps.com/index.php?opl=config_net.html>`__.
| . `Welcome to the Underground
  blog <https://versatile1.wordpress.com/2010/03/15/how-to-boot-games-off-network-smb-with-playstation-2-ps2-using-openps2loader-a-novice-guide/>`__.

----

*Windows Vista :*
-----------------

Seriously, is someone still using Vista ? :P

----

*Windows 7 :*
-------------

**Sharing your PS2 folder :**

| 1. Right-click on the folder you want to share, then go to “Share
  with” tab ;
| 2. Select “Specific people” ;
| 3. Choose “Everyone” and set properties for “Everyone” to
  “read/write”.

**Setting a share name :**

| 4. Right click on your shared folder, and go to “Properties”, and then
  “Sharing Tab” ;
| 5. Click on “Advanced Sharing” and then click on “Share this folder”.
| 6. Give share name the name PS2SMB (default name) – or any name you
  want, but it must match into OPL network configuration. Click OK.

.. image:: 4059816955-7_share.png
   :alt: title

**Setting your network profile :**

7. Now click on “Network and Sharing Center”(blue link as shown in the
picture above). Under the Public profile, please configure it as shown
in the screenshot below :

.. image:: 1130922764-7_settings.png
   :alt: title

| **Sources :**
| . `OPL 0.8 User
  Guide <http://opl.sksapps.com/index.php?opl=config_net.html>`__.
| . `Welcome to the Underground
  blog <https://versatile1.wordpress.com/2010/03/15/how-to-boot-games-off-network-smb-with-playstation-2-ps2-using-openps2loader-a-novice-guide/>`__.

----

*Windows 8 :*
-------------

Very similar to Windows 7 method. See
`here <http://www.dummies.com/computers/computer-networking/how-to-share-folders-and-documents-on-a-windows-8-network/>`__.

----

*Windows 10 :*
--------------

(to be completed)

----

*Mac OS X :*
------------

| 1. Open the “System Preferences” app.
| 2. Go to the “Sharing” folder.

.. image:: 1664414146-mac1.png
   :alt: title

3. In the list of services on the left side of the window, go to the
“File Sharing” item and click on the “Options…” button.

.. image:: 2748342783-mac2.png
   :alt: title

4. Enable the “Share files and folders using SMB” option and click on
the “Done” button.

.. image:: 4029471397-mac3.png
   :alt: title

5. Add the folder you want to share (ie. PS2SMB) to the “Shared Folders”
list by dragging and dropping it in the “Shared Folders” list and check
that “Everyone” has at least “Read Only” rights to this folder in the
“Users” list.

.. image:: 1833557120-mac4.png
   :alt: title

6. Your folder should be shared over SMB.

| **Source :**
| . `OPL 0.8 User
  Guide <http://opl.sksapps.com/index.php?opl=config_net.html>`__.
