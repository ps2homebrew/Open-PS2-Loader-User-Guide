**Official OPL 0.9.3+ Betas features**
======================================

Since this whole documentation is all about OPL 0.9.3 stable version –
this page will be dedicated to the Official OPL 0.9.3+ Betas features
that will be included in the next 0.9.4 stable version.

| You can download the Official 0.9.3+ Betas from Ifcaro repository
  `here <https://bitbucket.org/ifcaro/open-ps2-loader/downloads/OpenPS2Loader_0.9.3_Betas.zip>`__.
  You can give feedbacks/make reports about the new features in this
  `PSX-scene
  thread <http://psx-scene.com/forums/f150/open-ps2-loader-official-beta-revisions-releases-156209/>`__.
| If you are not using OPL in English, you can also download the updated
  language pack from
  `here <http://psx-scene.com/forums/f150/open-ps2-loader-official-compatibility-list-thread-156233/>`__
  .

**Notes :**

-  Not every commit made to Ifcaro repository bring a new feature – some
   are just little fix, code improvement, language update, some new
   features are committed in several commits (that’s why the reports
   from users are important). Don’t expect a comment for each commit. :P
-  Keep in mind that betas are WIP and that some new features can affect
   game compatibility. **0.9.3 should/must be your daily gaming OPL
   version**.

**New features :**

-  **rev927-rev930:** new In-Game-Screenshot (IGS) feature (see
   PSX-scene thread
   `here <http://psx-scene.com/forums/f150/opl-igs-game-screenshot-123872/>`__).
   How to make it work :

| . you need to use a OPL_GSM beta type version (IGS uses some GSM
  functions to work) ;
| . you need to have a mc inserted in slot 2 – your screenshots will be
  saved there ;
| . you need to enable GSM and disable IGR (mode 6 : OFF) in Game
  settings screen ;
| . do not make a screenshot while saving – loading a save ;
| . press the |R1| +\ |R2| + |L1| + |L2| + |up| hotkey in-game to
  capture a screenshot ;
| . if it worked, you are kicked back to PS2 broswer (you are stuck at a
  red screen color otherwise) ;
| . you can find your screenshot in the mc2 – saved as
  SLES_535.07_GS.dmp, SLES_535.07_SCR.bmp.
| Currently only 1 screenshot per game is supported – move them from mc
  before capturing again.

**Some screenshots :**

.. image:: https://s12.postimg.io/j38oqgwzh/SLES_535_07_SCRsmall.jpg

.. image:: http://psx-scene.com/forums/attachments/f150/58702-opl-igs-game-screenshot-scus_973.99_scr.bmp

.. image:: http://psx-scene.com/forums/attachments/f150/58716-opl-igs-game-screenshot-slus_207.12_scr.bmp

.. image:: http://psx-scene.com/forums/attachments/f150/58720-opl-igs-game-screenshot-slus_210.05_scr.bmp

-  **rev891-892 :** IGR color sequence reworked (debug mode). More info
   `here <http://psx-scene.com/forums/f150/open-ps2-loader-project-debug-colors-64354/index3.html#post1207452>`__.

(TODO: image file ``4004015801-DebugColors.png`` is missing)

-  **rev883 :** `PS3 BC(Backwards Compatible) network support
   fixes <http://psx-scene.com/forums/f150/possible-get-opl-work-decently-backwards-compatible-ps3-over-network-155082/>`__.

-  **rev882-rev896 :** new PS2 Logo feature. Allows to display PS2 logo
   at game startup. You need to enable this feature in the Display
   settings screen (set it to ON). The PS2 Logo will only be displayed
   if the game and your system belong to the same region – if not, PS2
   logo is not displayed. More info in this
   `thread <http://psx-scene.com/forums/f150/how-playstation-2-logo-after-starting-game-opl-156073/>`__.

-  **rev878-rev879 :** IGR path and Exit OPL doesn’t share the same exit
   path anymore. “Exit OPL ?” string had been renamed “Exit to
   Browser/OSDSYS ?” and “Leave empty to exit to Browser” renamed”
   “Boots Custom ELF after an IGR”. However, if you leave the Boots
   Custom ELF after an IGR setting as default (< not set >), you still
   exit OPL to PS2 Broswer. More info
   `here <https://bitbucket.org/ifcaro/open-ps2-loader/pull-requests/29/reverting-sysexecexit-unlinks-the-igr-and/diff>`__

-  **rev877 :** GSM version upgraded from 0.36.R to 0.38 – PS2RD
   compatible. (lister)

-  **rev853 :** not a new feature, but a fix. The function that creates
   OPL icon in mc#:/OPL folder was broken in 0.9.3 stable release –
   displaying blue cube (corrupted data). You can fix that manually by
   downloading opl.icn and icon.sys files from *Source / Open PS2 Loader
   / gfx /* in `Ifcaro
   repository <https://bitbucket.org/ifcaro/open-ps2-loader>`__ and
   replace the broken files by these.

.. |R1| image:: 3407914923-R1.png
.. |R2| image:: 2989855896-R2.png
.. |L1| image:: 359344587-L1.png
.. |L2| image:: 3537024755-L2.png
.. |up| image:: 3384562877-up.png
