**Widescreen (16:9) for PlayStation 2 games**
=============================================

**Note :** This can NOT be achieved using the “Widescreen” option from
OPL display settings page.

**Previews :**

.. image:: http://i.imgur.com/gYElt.giff
   :alt: title

*Final Fantasy X-2*

.. image:: http://www.abload.de/img/pcsx2-2012-09-09-23-1jsxm7.gif
   :alt: title

*Mortal Kombat: Shaolin Monks*

As you may know (or not), some PlayStation 2 games natively support 16:9
ratio. However,

-  there is no real standard about how to enable it : somes games
   required 16:9 to be enabled in PlayStation 2 system configuration
   menu to be displayed in widecreen ratio, while some others has their
   16:9 option in their own display settings menu (in game) ;
-  some games has their 16:9 ratio just skewed ;
-  some other games just doesn’t support 16:9.

It’s now possible to get proper 16:9 on a large amount of PlayStation 2
games. They are several methods to achieve this. Here’s 2 of them.

----

*Method 1 : patch the game image :*
-----------------------------------

.. image:: 2155596679-preview.png
   :alt: title

*PS2 Patch Engine tool*

Basic step-by-step :

| **(1)** – Create an image of your PlayStation 2 game, either as .iso,
  .img or .bin format ;
| **(2)** – Download `PS2 Patch
  Engine <http://psx-scene.com/forums/f19/ps2-patch-engine-117652/#post1088717>`__
  tool, by
  `pelvicthrustman <http://psx-scene.com/forums/members/pelvicthrustman/>`__
  ;
| **(3)** – Get a 16:9 patch for your PlayStation 2 game, either as
  \*.pnach file (see the `PCSX2 widescreen
  archive <http://forums.pcsx2.net/Thread-PCSX2-Widescreen-Game-Patches?pid=271674#pid271674>`__
  at the bottom of the post), either as RAW code.
| **(4)** – Read the “How to use it” section of this
  `post <http://psx-scene.com/forums/f19/ps2-patch-engine-117652/#post1088717>`__.
| **(5)** – Once done, install your PS2 game for use with OPL, like you
  would for any other games.
| **(6)** – Enjoy !

**Note :** WS .pnaches are game specific, which means you can’t apply a
NTSC-U .pnach over a PAL game and vice-versa (example).

----

*Method 2 : using OPL+PS2RD :*
------------------------------

Process is exactly the same as you would do for any other cheats codes –
except the fact you also need to convert 16:9 patches from .pnach to RAW
codes.

**Basic step-by-step :**

| **(1)** – Create a <game_ID>.cht text file, replacing <game_ID> with
  the actual ID of your game. Example – Okami (PAL) : SLES_544.39.cht.
| **(2)** – Extract the main executable of your PS2 game using `ELF
  Extractor <http://psx-scene.com/forums/f19/ps2-hacking-toolkit-116460/#post1080650>`__
  by
  `pelvicthrustman <http://psx-scene.com/forums/members/pelvicthrustman/>`__
  ;
| **(3)** – Use `MasterCode
  Finder <http://psx-scene.com/forums/f293/mastercode-finder-110898/#post1038200>`__
  tool, by
  `pelvicthrustman <http://psx-scene.com/forums/members/pelvicthrustman/>`__
  to determine the mastercode of your game ;
| **(4)** – Get a 16:9 patch for your PlayStation 2 game, as \*.pnach
  file (see the `PCSX2 widescreen
  archive <http://forums.pcsx2.net/Thread-PCSX2-Widescreen-Game-Patches?pid=271674#pid271674>`__
  at the bottom of the post) ;
| **(5)** – Convert your 16:9 patch (.pnach format) to RAW codes using
  `PNACH
  Converter <http://psx-scene.com/forums/f293/pnach-converter-2-01-a-110108/#post1031413>`__
  tool, by
  `pelvicthrustman <http://psx-scene.com/forums/members/pelvicthrustman>`__
  ;
| **(6)** – Write the mastercode and WS code in your <game_ID>.cht file,
  like this :

SLES_544.39.cht :

::

   Master Code
   9020FB28 0C0FBB2A
   Widescreen Code
   201974d4 3c014455
   20344864 3c014455

| **(7)** – Drop your <game_ID>.cht file in your CHT folder on the
  device you launch your games from (either +OPL/CHT, or mass:/CHT, or
  smb:/CHT) ;
| **(8)** – Launch OPL, enable PS2RD in the “Cheats settings screen”,
  and launch your game ;
| **(9)** – Enjoy !

**Note :** mastercodes and WS \*.pnaches are game specific : you can’t
use a PAL mastercode for a NTSC-J game, nor apply a NTSC-U .pnach over a
PAL game and vice-versa (example).

| **Sources :**
| . `PSCX2
  forum <http://forums.pcsx2.net/Thread-PCSX2-Widescreen-Game-Patches>`__
  – thanks to everyone who contributed to the archive ;
| . `Pelvicthrustman’s PS2 Hacking
  Toolkit <http://psx-scene.com/forums/f19/ps2-hacking-toolkit-116460/>`__
  by
  `pelvicthrustman <http://psx-scene.com/forums/members/pelvicthrustman/>`__
  – thanks for the great tools provided.
