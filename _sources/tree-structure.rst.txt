**OPL overview**
================

*OPL Configuration files :*
---------------------------

OPL will store its settings into 2 different configuration files –
conf_opl.cfg and conf_network.cfg – whereas OPL 0.9.2 used only one file
(conf_opl.cfg). OPL main settings and display settings will be saved
into conf_opl.cfg – while network config settings are saved into
conf_network.cfg.

Another difference with 0.9.2 is that conf_opl.cfg doesn’t store GSM
settings anymore – since GSM is now configurable per-game. These
settings, along with compatibility modes, VMC data… are now saved into
per-game specific files – named <game_IG>.cfg – and stored in the CFG
folder of the device you launch your games from.

conf_opl.cfg and conf_network.cfg will be read / loaded / saved in this
order (basically from the faster to the slowler device) :

**MC0 >> MC1 >> HDD >> USB**

If OPL fails to write or find its settings on MC, it looks on HDD for
them and etc…

If you want to save OPL settings into another device that the MC, remove
all MC from slots, disable all devices except the one you want to save
onto and “save changes” (don’t forget to remove your settings from
mc:/OPL folder if you had). At next launch, OPL will load your settings
from the device you choose (and save here), even if you have a MC
inserted in a slot.

For HDD, conf_opl.cfg and conf_network.cfg are stored in the root of the
+OPL partition ; for USB, they are stored in the root of the USB device.

**Note :** OPL folder – along with opl.icn and icon.sys – will still be
created on your mc, even if you choose to save your settings on another
device.

Any other file – which all are game related : ARTs, cheats, VMC... – can
not be stored on the MC – but only on the device you launch your games
from.

----

*Directory structure :*
-----------------------

OPL uses the same directory tree structure across HDD, SMB, and USB
modes. These folders will be automatically created when you launch OPL
for the first time and select and choose your main device (choose a
“start mode” in Settings screen). For HDD users, a 128Mb +OPL partition
will be created (of course, the CD and DVD folders will not be created).

**Directory tree structure :**

+-----------------+------------------------+------------------------+
| **Folder name** | **Usage**              | **Example**            |
+-----------------+------------------------+------------------------+
| CD              | For storing games on   | (my example isn’t an   |
|                 | CD media ( < 700Mb) –  | CD game :P )           |
|                 | i.e. blue-bottom discs |                        |
|                 | – named as My game.iso |                        |
|                 | (you no longer need to |                        |
|                 | use the Game ID in the |                        |
|                 | iso name).             |                        |
+-----------------+------------------------+------------------------+
| DVD             | For storing DVD5 and   | Okami.iso              |
|                 | DVD9 game images –     |                        |
|                 | named as My game.iso   |                        |
|                 | (you no longer need to |                        |
|                 | use the Game ID in the |                        |
|                 | iso name). These       |                        |
|                 | images, when over 4GB, |                        |
|                 | **must** be sliced     |                        |
|                 | into several parts if  |                        |
|                 | you use OPL in USB     |                        |
|                 | mode (due to FAT32     |                        |
|                 | limitation).           |                        |
+-----------------+------------------------+------------------------+
| VMC             | For storing Virtual    | SLES_544.39_0.bin      |
|                 | Memory Card images –   |                        |
|                 | usually named as       |                        |
|                 | <game_ID>_0/1.bin>.    |                        |
+-----------------+------------------------+------------------------+
| CFG             | For storing per-game   | SLES_544.39.cfg        |
|                 | configuation files –   |                        |
|                 | named as               |                        |
|                 | <game_ID.cfg>.         |                        |
+-----------------+------------------------+------------------------+
| CFG-DEV         | For storing per-game   | SLES_544.39.cfg        |
|                 | configuation files –   |                        |
|                 | named as <game_ID.cfg> |                        |
|                 | – *when saved from a   |                        |
|                 | OPL beta version*.     |                        |
+-----------------+------------------------+------------------------+
| ART             | For storing ART files  | SLES_544.39.COV.jpg    |
|                 | (coverboxes,           |                        |
|                 | backgrounds and icons  |                        |
|                 | disc images… – named   |                        |
|                 | as <game_ID.COV.jpg>   |                        |
|                 | (cover art).           |                        |
+-----------------+------------------------+------------------------+
| THM             | For storing custom     | `thm_Un                |
|                 | themes – named as      | iverse_9 <http://psx-s |
|                 | <t                     | cene.com/forums/f150/s |
|                 | hm_name_of_the_theme>. | hare-your-theme-art-op |
|                 |                        | lv0-9-beta-80461/index |
|                 |                        | 43.html#post996400>`__ |
+-----------------+------------------------+------------------------+
| CHT             | For storing cheats     | SLES_544.39.cht        |
|                 | files – named as       |                        |
|                 | <game_ID.cht>.         |                        |
+-----------------+------------------------+------------------------+

**Note :** the same suffix is used on all devices. Ex : cheat files are
always saved as <game_ID.\ **cht**>, no matter where they are stored in.
