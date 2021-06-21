.. _game_settings:

**Game settings screen**
========================

| ----
| *[Default values are marked in bold]*

**Note :** OPL 0.9.3 uses per-game configuration files. Instead of
storing in-game compatibility settings into a global configurations file
like in previous OPL versions, it now stores such data as compatibility
modes, VMC, and any applicable DNAS data inside per-game configuration
files named <game ID>.cfg (i.e. SCUSxxx_xx.cfg) which will be stored in
the CFG folder on the device your run your games from (either mass:/CFG
or smb:/your_shared_folder/CFG or hdd:/+OPL/CFG). If you are running an
official OPL 0.9.3+ beta, these <game ID>.cfg will be stored in a
CFG-DEV folder instead.

(TODO: image file ``2093241865-game-settings.png`` is missing)

**Game settings screen :**

-  **Compatibility Modes :**

Though OPL has a very high compatibility rate using the default
settings, some games might need a compatibility mode to run correctly.
Press the select button to enable (ON) or disable (OFF) a mode.

+----------+---------------------+---------------------+------------+
| **Mode** | **Mode name**       | **Description**     | **Device** |
+----------+---------------------+---------------------+------------+
| 1        | Accurate Reads      | Emulate the reading | All        |
|          |                     | performance and     |            |
|          |                     | behaviour of the    |            |
|          |                     | CD/DVD drive,       |            |
|          |                     | without ever        |            |
|          |                     | needing to use some |            |
|          |                     | slow transfer mode  |            |
|          |                     | like MWDMA mode 0.  |            |
|          |                     | Required by buggy   |            |
|          |                     | games that glitch   |            |
|          |                     | when exposed to the |            |
|          |                     | higher transfer     |            |
|          |                     | rates and the       |            |
|          |                     | synchronous nature  |            |
|          |                     | of HDD mode.        |            |
+----------+---------------------+---------------------+------------+
| 2        | Synchronous Mode    | Makes OPL read data | All        |
|          |                     | synchronously (read |            |
|          |                     | immediately upon    |            |
|          |                     | receiving the       |            |
|          |                     | request) instead of |            |
|          |                     | asynchronously (in  |            |
|          |                     | the background).    |            |
|          |                     | Reads will take     |            |
|          |                     | place immediately   |            |
|          |                     | from the calling    |            |
|          |                     | thread. Some games  |            |
|          |                     | will need this      |            |
|          |                     | because of their    |            |
|          |                     | design.             |            |
+----------+---------------------+---------------------+------------+
| 3        | Unhook Syscalls     | OPL will not remain | All        |
|          |                     | resident in EE RAM  |            |
|          |                     | after the game      |            |
|          |                     | resets the IOP with |            |
|          |                     | its IOPRP image.    |            |
|          |                     | Required for games  |            |
|          |                     | that can overwrite  |            |
|          |                     | OPL or can somehow  |            |
|          |                     | confuse OPL’s       |            |
|          |                     | SifSetDma hook.     |            |
|          |                     | When this mode is   |            |
|          |                     | used, mode 6        |            |
|          |                     | (disable IGR) must  |            |
|          |                     | be disabled. GSM    |            |
|          |                     | and PS2RD cannot be |            |
|          |                     | used either.        |            |
+----------+---------------------+---------------------+------------+
| 4        | 0 PSS mode          | Changes the         | All        |
|          |                     | reported sizes of   |            |
|          |                     | PSS video files to  |            |
|          |                     | 0 (make .PSS files  |            |
|          |                     | dummies), so that   |            |
|          |                     | they will be        |            |
|          |                     | skipped. Useful for |            |
|          |                     | slow devices like   |            |
|          |                     | USB and SMB. Useful |            |
|          |                     | if the game         |            |
|          |                     | contains a lot some |            |
|          |                     | PSS file you want   |            |
|          |                     | to skip . This mode |            |
|          |                     | fixes some games    |            |
|          |                     | that freezes due to |            |
|          |                     | timing issue with   |            |
|          |                     | videos (Max Payne). |            |
+----------+---------------------+---------------------+------------+
| 5        | Emulate DVD-DL      | Emulates DVD-DL for | All        |
|          |                     | flatterned DVD9     |            |
|          |                     | images to DVD5      |            |
|          |                     | image using rip     |            |
|          |                     | kits. DVD-DL        |            |
|          |                     | support must be     |            |
|          |                     | emulated because    |            |
|          |                     | OPL will otherwise  |            |
|          |                     | treat such a disc   |            |
|          |                     | image as a regular  |            |
|          |                     | single-layer disc.  |            |
+----------+---------------------+---------------------+------------+
| 6        | Disable IGR         | Disable In-Game     | All        |
|          |                     | Reset (IGR). IGR    |            |
|          |                     | may cause problems  |            |
|          |                     | for some games,     |            |
|          |                     | hence disabling it  |            |
|          |                     | may be necessary.   |            |
+----------+---------------------+---------------------+------------+
| 7        | High module storage | For games that need | All        |
|          |                     | OPL to store its    |            |
|          |                     | modules elsewhere,  |            |
|          |                     | to avoid a memory   |            |
|          |                     | conflict (Fatal     |            |
|          |                     | Frame). Meant to    |            |
|          |                     | shift the module    |            |
|          |                     | storage of OPL from |            |
|          |                     | 0×00097000          |            |
|          |                     | to 0×01C00000.      |            |
+----------+---------------------+---------------------+------------+
| 8        | Hide DEV9 module    | A bit like “Disable | All        |
|          |                     | Network support”    |            |
|          |                     | mode of some HDL    |            |
|          |                     | versions. For HDD   |            |
|          |                     | mode, CDVDMAN       |            |
|          |                     | reports itself as   |            |
|          |                     | “dev9” so that      |            |
|          |                     | games with network  |            |
|          |                     | support will not    |            |
|          |                     | lose their network  |            |
|          |                     | support. But it     |            |
|          |                     | appears that some   |            |
|          |                     | games like Need for |            |
|          |                     | Speed: Underground  |            |
|          |                     | 2 will not work if  |            |
|          |                     | dev9 is visibly     |            |
|          |                     | resident.           |            |
+----------+---------------------+---------------------+------------+

**Note :** some compatibility modes changed since OPL 0.9.2 – and some
even changed during 0.9.3 developpement.

----

-  **Configure GSM :** leads you to GSM screen page – will allow you to
   force video modes in-game. Read more about GSM
   :ref:`here <gsm>`.

-  **DMA mode :** < **no values** / (see list below) > – allows you to
   set the transfer mode that will have an impact on HDD reading speed.
   It may help some problematic games to run better. Indeed, some
   (buggy) games break down when data is transferred at a higher rate.
   Not available for USB and ETH games.

+----------+-----------+---------------------------------------------+
| **Mode** | **Speed** | **Note**                                    |
+----------+-----------+---------------------------------------------+
| UDMA-4   | 66MB/s    | Internal HDD default reading speed.         |
+----------+-----------+---------------------------------------------+
| UDMA-3   | 44MB/s    |                                             |
+----------+-----------+---------------------------------------------+
| UDMA-2   | 33MB/s    |                                             |
+----------+-----------+---------------------------------------------+
| UDMA-1   | 25MB/s    |                                             |
+----------+-----------+---------------------------------------------+
| UDMA-0   | 16MB/s    |                                             |
+----------+-----------+---------------------------------------------+
| MDMA-2   | 16MB/s    |                                             |
+----------+-----------+---------------------------------------------+
| MDMA-1   | 13MB/s    |                                             |
+----------+-----------+---------------------------------------------+
| MDMA-0   | 4MB/s     | MDMA mode 0 offers the closest transfer     |
|          |           | rate to the CD/DVD drive’s transfer rate,   |
|          |           | although it is still a little faster.       |
+----------+-----------+---------------------------------------------+

----

-  **VMC screen section :** allow you to create a VMC file or assign /
   configure an existing one to a selected game. Read more about VMC
   `here <https://bitbucket.org/ShaolinAssassin/open-ps2-loader_documentation-project-do-not-delete/wiki/vmc>`__.

----

-  **Game ID :** < **not set** / > – press the select button without a
   disc in the tray and you can input a Game ID for online DNAS
   authentication. You can not play Online from Network Games, since the
   network is already in use to run the game.

-  **Load from disc :** allows you to get the ID from your original game
   disc by inserting the disc in the tray and pressing the select
   button.

----

-  **Custom ELF :** < **not set** > – this option lets you define a path
   to a custom ELF within multi-ELF games, compilations, and PS2 Demo
   discs. You can enter whatever ELF name is required to launch the
   demo/game. This is only needed when the startup ELF inside the ISO is
   NOT THE SAME as the game prefix (ex: SCES_xxx_xx). For example, the
   well known 4 Edges demo has a startup ELF named “4EDGES.ELF’. In that
   case, name the ISO as “The Black Lotus – 4 Edges.iso” and then put
   “4EDGES.ELF” as the custom ELF.

----

-  **Save changes :** will save any changes you made on this screen.

-  **Test :** allows you to try a mode/setting without saving it. Runs
   the game immediately.

-  **Download defaults :** allows you to download defaults records
   reported by users from `OPL-CL
   site <http://sx.sytes.net/oplcl/games.aspx>`__ (<game ID>.cfg files
   including compatibility modes, settings, game data…). Read more about
   this in the :ref:`Network update section <network_update>`.

-  **Remove all settings :** will revert all the settings to the default
   settings and auto-save.

----

-  |title| or |image1| (according to the select button you choose in the
   settings screen) – returns you to the previous screen without any
   changes made.

.. |title| image:: 74665754-cross.png
.. |image1| image:: 4184835271-circle.png
