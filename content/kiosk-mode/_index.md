+++
title = "Kiosk Mode"
weight = 600
sort_by = "weight"
insert_anchor_links = "right"
+++

{% note() %}
Nothing in this section is specific to being in a planetarium! You can install
WWT in kiosk mode anywhere you’d like.
{% end %}

AAS WorldWide Telescope can be launched in a kiosk mode, which is designed for
unfacilitated use in museums or other informal learning environments. There
are two general ways this can be done. One is to show a narrative presentation
in the form of a tour. The other mode is to allow free exploration.

Unless you go to great lengths to harden your kiosk computer by installing
software to intercept certain Windows keyboard commands, you should not have a
publically-accessible keyboard connected. A connected keyboard gives the user
the ability to Control-Alt-Delete to get task manager, which could break out
of WWT and give access to the computer. For administration purposes, museum
staff will want to be able to connect a keyboard or remote desktop to the
computer to do this.


# Kiosk Tours

1. Create or open your tour in WWT. Save it to a file at a folder on your PC.
2. On the last slide of your tour Right-click and choose “Set Next Slide.”
   This will bring up a dialog box click the first slide of the tour. Clicking
   the slide will also check the box “Link to Slide (Selected below).” Click
   OK.
3. Create a shortcut.
   1. Right-click at the location you want the shortcut to live and select
      “New/Shortcut”
   2. This will open a dialog box to type the location of the item. You can
      browse to the WWT install or if it is a standard installation, you can
      enter `C:\Program Files (x86)\Microsoft Research\Microsoft WorldWide
      Telescope\WWTExplorer.exe`. Don’t forget that the entire path should be
      enclosed in double quotes.
   3. Following the location for `WWTExplorer.exe` (which is the WWT
      application), you should put the location of the Kiosk Tour you created
      in the first step. In this example, the tour (named `Kiosk Tour.wtt`) is
      on the desktop for the user named Exhibit and the full path to the tour
      `C:\Users\Exhibit\Desktop\Kiosk Tour.wtt`.
   4. Following the path to the tour, put the flag that puts the application
      into the kiosk mode `-kiosk`.
   5. For the above example, the entire entry for the location of the item
      would be: `"C:\Program Files (x86)\Microsoft Research\Microsoft
      WorldWide Telescope\WWTExplorer.exe" "C:\Users\Exhibit\Desktop\Kiosk
      Tour.wtt" -kiosk`. When you are finished you might want to change the
      name of the shortcut to something relating to the tour, such as “Run
      Cool WWT Kiosk Tour,” otherwise it will default to the name
      “WWTExplorer.exe”.
   6. You can always change this by right-clicking on the shortcut and
      selecting “Properties”. In the dialog box that comes up you can edit the
      Target field.


# Interaction in Kiosk Tours

In all cases you should consider what interaction you want with the public to
have with WWT. Possibilities are:

* Mouse/trackball
* [XBox controller](@/controllers/_index.md)
* Touch screen


# Auto-starting Tours on Startup

1. Setup auto-login for user running WWT.
2. Setup shortcut to be executed on login
