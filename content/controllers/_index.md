+++
title = "Controllers and Virtual Buttons"
weight = 300
sort_by = "weight"
insert_anchor_links = "right"
+++

MIDI (Musical Instrument Digital Interface) is a protocol for connecting
commodity controllers, such as MIDI keyboards, control panels, foot pedals or
any other MIDI capable USB device. WWT provides a setup panel for users to map
keys, buttons, knobs, sliders and foot pedals to nearly all of WWT
functionality. Similarly, WWT allows custom mapping to an Xbox game
controller. This functionality can be used in classroom presentations,
planetarium control boards, in museum settings, and for data exploration with
temporal and other controls.

Currently, the AAS WorldWide Telescope Windows client can be controlled by a
variety of controllers. Custom mapping can be done for MIDI and Xbox
controllers, connected by USB to the computer running WWT as well as
configurable virtual buttons.


# MIDI Controllers

Any MIDI controller can be used to control WWT. You can re-use mapping of WWT
functions created by someone else. You can also create your own or edit a
previously-created mapping. Start by selecting {{ui(p="Settings > Controller
Setup ...")}}. This brings up a dialog window where you can select a file
containing the mapping functions. For the Numark DJ2Go you can
[download a standard mapping file](./Numark%20DJ2Go.wwtmm).

![Numark DJ2Go](numark_djtogo.jpg)

You can save and load different files with different mappings.

Highlighting a device in the list of MIDI devices on the left and clicking
“Properties” below will bring up the Controller Properties window that
presents the status of the controller and location to the image file used for
mapping. Note, that this image can be specified as a URL or a local file, such
as `C:\Documents\MIDI\numarkdj2go.png`.

To remove an existing binding, select it in the list and click the “-” button.
A box will come up to ask you to confirm the removal of the control.

To add a new binding, click the “+” button. This will bring up a box saying
that WWT is listening to the controller waiting for you to
manipulate a control that has not been previously mapped. When such a control
is moved, it will ask for the control type; select one of:

* **KeyPress** — detects that a key has been pressed and does some action.
* **KeyUpDown** — this sets up two actions, one when the key goes from Down to
  Up and the other from Up to Down. These can be defined separately.
* **Slider** — linear slider from one value to another
* **Knob** — rotating know from one value to another
* **Jog** — jog dial that can be move spun repeatedly, often used in advancing
  time

Once you have selected the control type it will be added to the list of
control bindings with the Control Name the same is the ID number. You can then
define what you want to happen when you manipulate the control. When you
select a control binding the properties are shown below the list and you can
change or set the following properties:

* **Binding Target Type pull-down** — Categories of actions that can be sent
  to WWT.
* **Bind Type pull-down** — Ways to bind the controller to WWT.
* **Property pull-down** — Specific properties controlled.
* **Repeat checkbox** — If this is checked, holding down will continuously
  send the same command. This makes sense for actions like zooming.

A full list of potential bindings is available in
[this Excel spreadsheet](./wwt-midi-binding-properties.xlsx).

The labels for the functions can be placed on the position of the
corresponding knob on the image for the controller. In the case of the default
map this has already been done. Click the function in the list and hold and
drag onto the image. Release your mouse when the label is at the desired
location. Note that when the “Monitor” box is checked and the key is pressed
on the controller the label changes from white to yellow.


# Xbox Controllers

WWT can be controlled by a PC version of a Microsoft XBox controller. This is
an excellent interface to use in a planetarium or presentation environment
because the controller is portable and the buttons can be distinguished in the
dark.

WWT comes with a standard binding of functions. This default is for the
left/right triggers to zoom out/in. The right bumper steps through objects in
the context menu (at the bottom of WWT screen). The left thumbstick pan and
scroll and the right thumbstick rotates the view. The Back key steps backwards
and the Start key steps forwards through LookAt modes (Sky, Earth, SolarSystem
etc.). The ABXY keys are defined in the table below.

| Button | Earth Mode | Sky Mode | Solar System Mode |
| :-- | :-- | :-- | :-- |
| **A** | | Equatorial Grid | Asteroids |
| **B** | | Constellation Boundaries | Milky Way Model |
| **X** | Clouds | Ecliptic Overview | Planetary Orbits |
| **Y** | Clouds | Constellation Figures | 3D Stars |

A table of the default mappings appropriate for print or reference is
available [here](./Xbox%20Controller%20Mapping.pdf).

In order to define your own settings select {{ui(p="Settings > Xbox Controller
Setup...")}}. This brings up a dialog window where you can select a file
containing the mapping functions. Check the “Use Custom Mappings” box and you
can see the default mapping and change any of them. You can control the
properties in the same way as the MIDI controller, described above. Checking
the “Use Mode Dependent Mappings” allows a different mapping to be used
depending on the mode.

You can save, load and share custom mappings files (extension `.wwtxm`) from
this dialog box.


# Virtual Buttons

Clicking the View button will show the View controls at the top of the WWT
window. The blank area to the right of the control – identified by the green
box in the image below – is a place where you can define and place custom
virtual buttons. These buttons can have the same bindings as the MIDI and Xbox
controllers.

![Numark DJ2Go](virtual_buttons.jpg)

Clicking the “+” key brings up a binding dialog box. You can give the button a
“Name,” select “Button Type,” “Binding Target Type,” “Bind Type,” and
“Property,” just like the MIDI controller, described above.

In the example above I have defined a Longitude and Latitude slider. Clicking
the “E” enters an editing mode for the buttons. When in edit mode, you can
rearrange the buttons. Right clicking on a button will allow you to toggle the
button editing mode, change the binding properties or delete a virtual button.
