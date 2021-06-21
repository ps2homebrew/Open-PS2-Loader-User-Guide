**In-Game-Reset**
=================

OPL features In-Game-Reset – IGR for short. This feature allows you to
quit a game, return to the games page and select another game to play,
choose a different application to run , go to the system main screen or
power-down your system without needing to get up and touch it. IGR is
enabled by default for all games – but you can disable it if you want.

-  Pressing |L1| + |L2| + |R1| + |R2| + |select| + |start| *in-game*
   will stop a game and launch the ELF you set for IGR path for [Menu >
   Settings to set an IGR path]. Only MC paths (example :
   mc0:/BOOT/BOOT.ELF) are supported.

-  Pressing |L1| + |L2| + |L3| + |R1| + |R2| + |R3| *in-game* will
   power-off the console, placing it in stand-by mode.

**Notes :**

-  Not every game is going to work with IGR, as some games have a
   similar option or are not compatible with IGR and some games may not
   work at all unless IGR is disabled. You can disable the IGR function
   in the Game settings screen by setting Mode 6 to ON.
-  If IGR isn’t working, you can try to find the issue by enabling the
   debug color [Settings screen]. If you are stuck at a red screen, it
   usually means a failure to load the ELF you choose as an IGR exit
   option. Check the path of your ELF, or if the ELF file is not either
   bad or missing.

**IGR debug colors sequence
(explained**\ `here <http://psx-scene.com/forums/f150/open-ps2-loader-official-compatibility-list-thread-156233/index2.html#post1208413>`__\ **)
:**

::

   White - Start of initialization of SIFCMD and SIFRPC
   Dark Blue - Start of SPU initialization
   Red - Start of IOP reboot, removal of kernel hooks, reinitialization of TLB (for GTA/GT4) and stopping of performance counter (for GT4).
   Green - Uninstallation of GSM
   Blue - Uninstallation of the cheat engine
   Yellow - Start of synchronization with IOP boot
   Pink - Start of (re-)initialization of SIFCMD and SIFRPC
   Dark Geen - Deinitialization of SIFRPC and SIFCMD
   If the target is an ELF, then (otherwise, just invoke the Exit syscall) - ELF Loader codes:
   Blue-Green: (re-re-)initialization of SIFCMD and SIFRPC.
   Dark Red: Start of SBV patch to enable the LoadModuleBuffer RPC function
   Sky-Blue: Load rom0:SIO2MAN, rom0:MCMAN and the target ELF.
   Orange: Start of ELF execution
   Red: Failed to load ELF (i.e. bad/missing file)

.. |L1| image:: 359344587-L1.png
.. |L2| image:: 3537024755-L2.png
.. |R1| image:: 3407914923-R1.png
.. |R2| image:: 2989855896-R2.png
.. |select| image:: 3991913910-select.png
.. |start| image:: 568074192-start.png
.. |L3| image:: 697506606-L3.png
.. |R3| image:: 2935175956-R3.png
