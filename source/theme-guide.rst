**Theme guide**
===============

OPL main GUI is composed of an ordered list of **elements** drawn
starting from the element at index 0 to the last element (max num). The
elements are named “main” followed by their order prefix:

::

   main0
   main1
   ...

The element **numbering must be consecutive** (i.e no missing number in
the middle, or OPL will ignore your last elements).

The minimal layout must have at least a *Background*, and the
*ItemsList*. If you omit them, they will be added automatically for you
with default attributes. The **Background** must be the lowest element
of the list ! If you try to add a Background at some other position, it
will be ignored (and a new default Background will be create instead at
position 0), so be sure sure to define your own background as first
element.

Each elements have the same set of basic **attributes**, and then some
have their own specific attributes. Basic attributes have default
values, so you can (but it is not necessarily a good idea) omit to
define them in your conf_theme.cfg. Any attributes declared in the
conf_theme.cfg override the default.

----

*Attributes*
------------

Let’s start to describe the basic attributes (refers to the `official
OPL 0.8 guide <http://opl.sksapps.com/index.php?opl=theme.html>`__ for
more information):

-  **enabled**: Boolean, define if your element is enabled or not.
   Enabled by default.
-  **type**: String value taken from the enumeration of available
   elements (see below). This attribute is mandatory, if it is not
   present or invalid (beware it is case sensitive) your element will be
   completely ignored.
-  **x**: Integer, define the X position of your element, default is 0.
   If you want to dispose your element exactly in the middle of the
   screen, use the String value of “POS_MID”.
-  **y**: Same as above, but for the Y position.
-  **width**: Integer, define the width of your element, default is to
   use the size of the element (image/text) itself. You can force/resize
   it with this attribute.
-  **height**: Same as above but for height.
-  **aligned**: Alignment mode, refer to original guide. Default is
   usually the expected value, so omit it.
-  **color**: Color used for element that contains “text”. Default is to
   use the “text_color” of your theme. String of type “#RRGGBB”. Refers
   to original guide.
-  **font**: Integer. Font used for element that contains “text”. Can
   either use the theme default, or OPL default (set in the “Display
   settings”). Read more below.

----

*Elements*
----------

Now the list of elements:

-  **MenuIcon**: Top left menu icon. No specific attributes.
-  **MenuText**: Top middle menu description. No specific attributes.
-  **ItemsList**: Contains the list of items (games/apps).
-  **Attribute items**: Integer, describe how many items you want to
   display at most. Same as the old theme setting “displayed_items”.
   Default value is calculated depending of the screen height.
-  **Attribute decorator**: String. You put here the pattern attribute
   of a GameImage element you have define in your conf_theme.cfg and you
   want to use as decorator for each items. This is to replace the old
   theme setting “items_list_icons” which was adding by default the Item
   Icon in front of each item. If no present, there will be no
   decoration.
-  **ItemIcon**: Some alias to provide the old item icon functionality.
   This element is in fact a GameImage element with some hard-coded
   attribute values (pattern=ICO, default=disc, cache=20). Read below
   the GameImage description for specific attributes.
-  **ItemCover**: Alias for old item cover functionality. This element
   is a GameImage element with hard-coded attribute values (pattern=COV,
   cache=10).
-  **ItemText**: Display the current item startup elf. No specific
   attributes.
-  **HintText**: Display the hints at bottom. No specific attributes.
-  **LoadingIcon**: Display the busy icon. No specific attributes.
-  **Background**: Define the background mode to use. Replace the old
   theme setting “background_mode”. It is a “mutable” element, depending
   of the attributes you use, it will either be a StaticImage (for mode
   BG_PICTURE), or a GameImage (for mode BG_ART).
-  **AttributeText**: Display a text string, corresponding of the
   specific value of the attribute for the current game. Can only be
   used in the information page.
-  **Attribute attribute**: String. The attribute bound to this element.
   Currently you have these predefined internal attributes: #Media,
   #Format, #Name, #Startup, #Size.
-  **AttributeImage**: Display a picture, whom path is based on the
   value of the attribute for the current game. Can only be used in the
   information page.
-  **Attribute attribute**: String. The attribute bound to this element.
   Same as above.
-  **GameImage**: An element that display an image depending of the
   current item selected (using the gamecode as prefix).
-  **Attribute pattern**: String. This attribute is mandatory. It
   describe what suffix to append to the gamecode to find the image.
   Item icon/cover element above are using the default pattern of
   “ICO”/“COV” for example. You can add whatever you want (“SCR” for
   screen shot for example).
-  **Attribute count**: Integer. Define how many image OPL will cache
   for this element. Item icon/cover element use by default 30/10.
   Default is only 1. Beware with this settings, as if you are using big
   image for this element and a big cache, OPL will undoubtedly crash in
   out of memory. Moreover if you use a lot of GameImage elements.
-  **Attribute default**: String. Define the name of an optional picture
   to display when there is no corresponding picture for the current
   game. Without this attribute, there will be nothing drawn in that
   case. The picture is search inside your theme sub-folder. The name is
   without the extension (”.png” and “.jpg” will be tried).
-  **StaticImage**: An element that display a static image from your
   theme subfolder. Could be used as background, to include “frames” or
   to add any other fixed picture.
-  **Attribute default**: String. This attribute is mandatory. Name of
   your picture (inside your theme sub-folder), without the extension
   (”.png” and “.jpg” will be tried).

----

*About overlay*
---------------

The three main elements displaying image (GameImage, StaticImage and
later AttributeImage) support the use of overlay. Read the original
guide to see what it is exactly.

To add an overlay to your element, you just have to add these specific
attributes:

-  **overlay**: String. The name of the picture to use as overlay,
   located into your theme sub-folder. The name is without the
   extension, and **only “.png”** are accepted.
-  **overlay_ulx, overlay_uly, overlay_urx, overlay_ury, overlay_llx,
   overlay_lly, overlay_lrx, overlay_lry**: Integer, same as before with
   a little bit renaming (ul=upper left, ur=upper right, ll=lower left,
   lr=lower right).

----

*About Information page*
------------------------

Before running a game, you can display an information page about the
game. To define what is displayed, use the same syntax as for the “main
menu”, but use the “info” keyword instead:

::

   info0:
           type=Background
   info1:
           type=AttributeText
           attribute=#Name
           x=POS_MID
           y=25
   ...

----

*About background*
------------------

Here some example to help you defining your type of background.

To have the default (old) background displaying Art (BG_ART), using the
filename pattern of “SLUSXXX.YY_BG.png/jpg”, and if case of failure
using
“\ `background.png/jpg&#8221 <http://background.png/jpg&#8221>`__;, just
… don’t add any Background element to your config theme, OPL will add it
automatically.

To have a background displaying Art but using another ART pattern and
another default picture, use this:

::

   main0:
           type=Background
           pattern=FANART
           default=mycoolbackground

To have a background displaying only one static picture, use this:

::

   main0:
           type=Background
           default=mycoolbackground

To have the old plasma background, use this:

::

   main0:
           type=Background

To make your background fit both widescreen and standard ratios or even
PAL and NTSC:

::

   main0:
       type=Background
       pattern=BG
   main1:
       type=StaticImage
       default=mycoolbackground
       aligned=0
       scaled=0
       width=DIM_INF
       height=DIM_INF

----

*About fonts*
-------------

As this feature of Volca is also only present since the beta, it’s the
right place and moment to explain how it works.

By default all text elements of the GUI are using the global font
setting of OPL. Now when loading a theme, you can override this global
font with the theme attribute default_font. Now, this font will be used
by your elements. You can even define other multiple fonts, and assign
them to specific elements only, using the font attribute of each
element.

Here is a snippet showing how to define the fonts of your theme, using
the default_font attribute and an ordered list of filenames (this time
it’s a full path with extension) relative to your theme sub-folder:

::

   default_font=mymainfont.ttf
   font0=fontformenu.ttf
   font1=fontforhint.ttf
   [...]
   main3:
           type=MenuText
           font=0
   main4:
           type=HintText
           font=1

----

*Notes*
-------

When using “StaticImage”, those later are affected by the screen ratio
(wide-screen mode or not), which is usually a good thing. But when
putting a “frame” layer on top of the background, in this case you would
like to have it enlarged exactly like the background.

To achieve this result, you should use a picture of the same resolution
as your background (eventually with empty – alpha – region), and force
it’s size to “infinite” using the specific values “-1”.

::

   main0_type=Background
   main1:
           type=StaticImage
           default=frames
           width=-1
           height=-1

There is no “background_alt_mode” theme setting anymore … and there may
be no solution in the future …

-

When displaying the “info” page for a game, OPL will read this file, and
store the “key=value” pair. Then OPL will add automatically a few
internal attributes to this config set, which are prefixed by a “#”.

These are:

-  #Name : Contains the exact same name that is displayed in the
   standard list view
-  #Longname : only for APP, display the “long name”, i.e with full path
   for the application
-  #Media : contains either “CD” or “DVD”, depending of the game type.
-  #Format : contains one of “UL” / “ ISO” / “HDL”
-  #Size : the size in MB of the game
-  #Startup : the game ID code, as displayed in the standard view
