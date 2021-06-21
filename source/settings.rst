.. _settings:

**Settings screen**
===================

| ----
| *[Default values are marked in bold]*

You can access the Settings screen by pressing |start| from games/apps
pages then selecting Settings in the menu. This screen allows you to
configure main OPL settings.

(TODO: image file ``3234875202-settings.png`` is missing)

**Settings screen :**

-  **Disable Debug Colors :** < **Off** / On > – disables the color
   screens while games are loading if set to ON. If you are
   experimenting an issue that compatibility modes can not solve, you
   can try to enable it. If you are stuck at a white color during the
   game boot, it usually means a failure to load the main ELF of your
   game (usually due to a bad disc image). You can either : rename the
   .iso using the old naming syntax (<game_ID>.Name of your game.iso) –
   works only for a very few games and only for USB and ETH modes – or
   make a new image of your game (check it’s MD5 checksum after and be
   sure that it matches against MD5 checksum from redump.org). Any other
   color means a failure in OPL initialization (**uncorrectable errors
   for the user**) and should be reported in the `main OPL
   thread <http://psx-scene.com/forums/f150/open-ps2-loader-project-v0-9-3-a-62141/>`__
   so they can be taken care by the developers.

More info about debug colors
`here <http://psx-scene.com/forums/f150/open-ps2-loader-official-compatibility-list-thread-156233/index2.html#post1208413>`__.

-  **IGR Path :** < **not set** > – allows you configure a path to an
   ELF for OPL to launch upon Exit OPL [main menu] or from an IGR reset
   (in-game). Leave this blank to exit/IGR to Browser/OSDSYS. Only MC
   paths (example : mc0:/BOOT/BOOT.ELF) are supported. Note : you can
   set IGR to load OPL again – just keep in mind that it might cause
   some compatibility issue. Read
   `here <http://psx-scene.com/forums/f150/open-ps2-loader-compatibility-list-site-132906/index11.html#post1210303>`__.
   For these games, you can deny IGR by enabling “Mode 6 – Disable IGR”.

-  **Enable write operations :** < **Off** / On > – when set to ON,
   allows you to display the rename and delete options on screen from
   the Hint menu on each list. Disable it (OFF) to prevent accidental
   renaming or deletion. When write operations is disabled, the VMC
   options to configure an existing VMC (change its size or delete) are
   disabled too. You need to set it to ON to be able to access HDL
   server.

-  **Remember last played game :** < **Off** / On > – when set to ON,
   the last selected game will be the first in the displayed listing
   each time you return to the games list. You can also set a countdown
   to autolaunch this last selected game (in seconds, from 9 to 1 – 0 to
   disable autolaunch).

----

-  **Check USB Game Fragmentation :** < **Off** / On > – allows OPL to
   warn you if games on your USB devices are too fragmented to launch.
   Recommended setting is ON. This is NOT a workaround to not defragment
   your USB devices.

-  **USB and ETH Prefix Path(s) :** < **not set** > – allows you to
   configure multiple share paths to USB or ETH based devices, and
   troubleshoot some picky NAS devices that may add a sub-path to a
   share. This is also useful for people wanting to use the same
   external USB device either connected on their NAS and accessed
   through SMB, or directly (in traveler mode) to the PS2. Usually NAS
   don’t allow to share the “root” of the device, so you have to put
   your games into, let’s say a “PS2SMB” folder. When using this same
   device in USB mode, simply enter “PS2SMB” as USB prefix and you’re
   good. (The prefix is limited to 32 characters).

-  **Automatic HDD spin down :** **20** – this option allows you to
   specify an idle time-out of an HDD before it automatically spins
   down. The value is in minutes with a 20 minute max. If set to 0, the
   automatic spin-down is disabled and the HDD won’t be stopped – not
   even when using IGR.

----

By default all devices are disabled and OPL will not enable/display any
devices until you set them to.

-  **USB device start mode :** < **Off** / Manual / Automatic >
-  **HDD device start mode :** < **Off** / Manual / Automatic >
-  **ETH device start mode :** < **Off** / Manual / Automatic >
-  **Applications start mode :** < **Off** / Manual / Automatic >

-  **OFF** – removes the device from being selectable from the menu bar
   in the games pages. Recommended if you’re not using this device.
-  **MANUAL** – allows the device to be selectable from the menu bar in
   the games pages, but will not enable the device until the selected
   button is pressed. Can be useful if more than one device is used).
-  **AUTOMATIC** – automatically enables the device at boot and makes it
   selectable from the menu bar in the games pages. The appropriate
   setting for your main device.

-  **Default menu :** < **no value** > – choose the page you want OPL to
   display on startup [USB Games / Network games / HDD games]. You can’t
   choose apps page as your default menu.

----

-  Press **OK** to validate the changes and exit this screen – or press
   |title| or |image1| (according to the select button you choose in the
   settings screen) – to go back to the previous screen without any
   changes made.

.. |start| image:: 568074192-start.png
.. |title| image:: 74665754-cross.png
.. |image1| image:: 4184835271-circle.png
