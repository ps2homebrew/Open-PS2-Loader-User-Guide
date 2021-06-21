**Using ARTs**
==============

Open PS2 Loader 0.9.3 supports the use of ARTs for PS2 games. This
feature is disabled by default, so you need to enable it before using it
[Menu > Display settings > Enable cover art > ON]. You also need to
enable the device you launch your games from, otherwise your ARTs won’t
be loaded. Then you need to store your ARTs in the ART folder. If you
use several devices, you need to copy/paste your ART folder (and its
content) on all of them.

**List of supported ARTs :**

+---------------+------------------+-------------------------+--------------------------+--------------------------+-------------------------+
| **Type**      | **Default size** | **Format(s) supported** | **Syntax**               | **Okami example**        | **Default GUI support** |
+---------------+------------------+-------------------------+--------------------------+--------------------------+-------------------------+
| Front cover   | 140×200          | .jpg/.png               | <game_ID>_COV.format     | SLES_544.39_COV.jpg      | Yes                     |
+---------------+------------------+-------------------------+--------------------------+--------------------------+-------------------------+
| Icon disc     | 64×64            | .png                    | <game_ID>_ICO.format     | SLES_544.39_ICO.png      | Yes                     |
+---------------+------------------+-------------------------+--------------------------+--------------------------+-------------------------+
| Background    | 640×480          | .jpg/.png               | <game_ID>_BG.format      | SLES_544.39_BG.jpg       | Yes                     |
+---------------+------------------+-------------------------+--------------------------+--------------------------+-------------------------+
| Game screen 1 | (none)           | .jpg/.png               | <game_ID>_SCR1.format    | SLES_544.39_SCR1.jpg     | No                      |
+---------------+------------------+-------------------------+--------------------------+--------------------------+-------------------------+
| Game screen 2 | (none)           | .jpg/.png               | <game_ID>_SCR2.format    | SLES_544.39_SCR2.jpg     | No                      |
+---------------+------------------+-------------------------+--------------------------+--------------------------+-------------------------+
