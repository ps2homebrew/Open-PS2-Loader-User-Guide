Open PS2 Loader 0.9.3 – User Guide
==================================

| ----
| *[Warning : this is not OPL official repository, only a user guide for
  it. If you are interested in OPL src code, you can find
  it *\ `here <https://github.com/ifcaro/Open-PS2-Loader>`__\ *]*

.. image:: http://orig12.deviantart.net/bcd2/f/2016/279/6/4/for_dummies_by_shaolinassassin-dak4oda.gif
   :alt: dummies

*About Open PS2 Loader :*
-------------------------

Open PS2 Loader (OPL) is a 100% Open source game loader for the PS2 and
PS3 units. Open PS2 Loader can load games though USB, network (SMB) and
from the PS2’s HDD unit. It supports all models of the PlayStation 2,
and the PlayStation 3 models with PlayStation 2 backward compatibility.

*Downloads :*
-------------

-  **OFFICIAL OPL LATEST STABLE VERSION :** `Open PS2 Loader
   0.9.3 <https://bitbucket.org/ifcaro/open-ps2-loader/downloads/OpenPS2Loader_0.9.3.zip>`__

::

   ==== Version 0.9.3 / rev851 ====
   CORE:
   * New RDB-based DECI2 Debugging System.
   * Refactored and optimized core modules.
   * New CDVDMAN streaming mechanism for better performance.
   * Kinder, gentler, and hopefully better IGR mechanism
   * Added support for the DTL-T10000, for debugging.
   * Updated USB drivers - support drives greater than 1TB but less than 2TB in capacity, plus better reliability.
   * Eliminated the need for user-configurable delays in USB support.
   * Improved performance and stability of SMB support.
   * VMC Fix - Slot2 should no longer clone Slot1 and vice versa
   * Removed obsolete Compatibility Modes and needless GSM video modes.
   * New PS2RD Cheat Engine port by Doctorxyz.
   * Per-Game GSM Support.
   * New super-slim EE core, making mode 1 (Alt EE core) obsolete.
   * Added Accurate Reads mode, for emulating the reading speed and behaviour of the CD/DVD drive.
   * The CallBack Timer (CBT) setting now uses a standardized value and was merged into Accurate Reads mode.
   * Added a workaround for some clone network adaptors.
   * Mode 7 "IOP threading hack" removed, as the new streaming mechanism has taken care of all related issues.
   * New compatibility mode: "high module storage". For games that need OPL to store its modules elsewhere, to avoid a memory conflict.
   * Improved reading performance of the cdrom device.
   * Improved reliability of some CDVDMAN functions, for more consistent behaviour.
   * Improved DVD-DL support.
   * Changed "Disable DVD-DL" to "Emulate DVD-DL" to better explain what it does. It's to emulate DVD-DL support, for DVD9 rips (games with their 2 layers compacted into 1).
   * Fixed support for SMB usernames and passwords that are longer than 16 characters (limit extended to 31).
   * Fixed renaming functionality for USBExtreme games.
   * Various fixes for games.
   GUI:
   * Improved the behaviour of the auto-refresh option.
   * GSM moved to Game Options menu since its a Per-Game option now.
   * Infamous "Blockhead Grande" theme bug SQUARSHED! (Themes should now get loaded correctly, regardless of display settings).
   * New logo design by Berion, new changed icons by El_Patas.
   * Better error reporting and help messages in general.
   * Network settings are now saved in opl_network.cfg.
   * Improved stability, design and UI responsiveness.
   * Added missing icon hints.
   * Fixed the problem with the HDLDump server being difficult to shut down properly.
   * Fixed HDD corruption caused by deleting a game from the HDD unit.
   * Added a new network update mechanism, which allows game compatibility records to be automatically downloaded from the OPL-CL service.
   * SMB server can now be specified by its NetBIOS name.
   * IP address configuration can be set automatically with DHCP, although it is still recommended to reserve an IP address for the PS2 in the network because the DHCP reservation will not be ever renewed while in-game.
   * Renamed "Enable Delete and Rename" to "Enable Write Operations".
   * Changed the delete and modify VMC controls to be disabled instead of hidden, when writes are disabled.
   * ISO disc images no longer strictly need to be named in a special format. Simply put your ISO files in your CD and DVD folders and OPL will find them.
   * Game history will now be updated; the "towers" behind the "SONY Computer Entertainment" boot screen should continue to grow.
   * Added support for OTF fonts.
   * Added support for fonts stored on the HDD unit (root of +OPL partition; hdd0:+OPL/) and USB device (root of device; mass0:/).
   GAME FIXES &#38; COMPATIBILITY IMPROVEMENTS:
   * New patch: Choujikuu Yousai Macross
   * New patch: Super Robot Wars IMPACT
   * Drive state of sceCdStandby has been changed to PAUSE: Check iTV
   * New patch: Ratchet and Clank: Up Your Arsenal
   * New patch: The Oneechanbara
   * New patch: The Oneechanpuruu
   * New streaming mechanism for better playability: Various BEMANI games
   * Initialization is performed for search functions: Lifeline

*Official OPL Thread / Forum :*
-------------------------------

-  **Open PS2 Loader Project – v0.9.3**
   @\ `PSX-SCENE <http://psx-scene.com/forums/f150/open-ps2-loader-project-v0-9-3-a-62141/>`__

*Table of contents:*
-------------------------

.. toctree::
   :maxdepth: 2
   :caption: Contents:

   Release types<overview>
   Directory tree structure <tree-structure>
   Navigation/controls <nav-controls>
   USB Games <usb-mode>
   ETH Games <eth-mode>
   HDD Games <hdd-mode>
   Game settings screen <game-settings>
   GSM <gsm>
   VMC <vmc>
   IGR <igr>
   Apps page <apps-page>
   Menu <menu>
   Settings <settings>
   Display settings <display-settings>
   Network config <network-config>
   Network update <network-update>
   HDL Server <hdl-server>
   Cheat settings <cheat-settings>
   ARTs <art>
   Theme gallery <theme-gallery>
   Theme guide <theme-guide>
   Related / useful stuff <related>
   Widescreen (16:9) for PlayStation 2 games – basic guide <widescreen>



Indices and tables
==================

* :ref:`genindex`
* :ref:`modindex`
* :ref:`search`
