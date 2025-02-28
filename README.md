Originally available at http://forum.rscnet.org/showthread.php?t=214673 (currently down with no known backup)
Then mirrored at https://www.angelfire.com/nm/neogeoinserts/hshifter/h_shifter.htm
Below is the original documentation (bear in mind some info may be outdated):

# FFShifter v1.0 BETA 0.

# Important:

# This is FFShifter v1.0 BETA 0.

This software comes with no warranties of any kind.

By installing this software you agree that you do so at your own risk and you
accept full responsibility for any damage caused by the use or installation of the
software.

The producer of FFShifter makes every effort to ensure the program is safe but
can not accept any responsibility whatsoever for personal injury or death that
may arise during the use of the software, or any damage of any kind to your
system including corrupted files, lost data or damage to hardware.

# 1) Introduction

FFShifter is utility program to simulate a car gear shifter with a Force Feedback
Joystick. Its main functionality is to send key strokes to the active window (usually a
racing or driving simulation). It is meant to be used by home-made gear shifters (with
gear shifting plates) which use FF Joysticks.
The original idea was to provide a program that would actually simulate the gear
shifting plate by constricting the joystick to move on predefined paths. Unfortunately,
FF Joysticks do not provide the functionality of exact positioning. If you apply two
constant forces in opposite directions, they cancel themselves out. Also, when you
apply a constant force, it moves the joystick all the way to the force’s direction
(depending on force of course). So the ideal use of FFShifter is with a FF Joystick and
a gear shift plate.
With some practice you can use FFShifter with only the joystick, but expect to have
some bad shifts. The reason behind it, is when a constant force is applied in one
direction (lets say 180 degrees – in the third gear), you get resistance trying to pull the
joystick back, but you don not have resistance to the left or right, so by the weight of
your hand it may slide to first gear (left) or fifth gear (right). Another reason for a bad
shift is when a constant force kicks in, if you do not hold strongly the joystick it may
end up on another gear. I hope you understand the programs limitations, and you find
it useful.


# 2) Installation

To install FFShifter, unzip the file into a suitable folder on your hard drive. You must
ensure that the directory structure is preserved by using the appropriate option in your
unzip utility. You will know that it has been correctly unzipped if you see other data
folders beside the FFShifter.exe program.

# 3) Running FFShifter

Double-click the program file FFShifter.exe. After you configure your options you
press start and then you run your racing sim. If your racing sim is using force
feedback on your joystick, you will feel that the joystick is free and you will loose all
FFShifter’s force feedback effects (it will still report key presses). You must configure
your racing sim not to use the FF Joystick, save, exit, and restart FFShifter.
Alternatively, you can execute FFShifter, get into your game, and when you are ready
to race, press the hot key that starts FFShifter (Ctrl+1). Some games may not allow
key presses to be pickup by FFShifter (like Richard’s Burns Rally); in this case try
using the “Start With Delay” button.

Note: Microsoft® DirectX® 8.1 is required and can be downloaded from
[http://www.microsoft.com/windows/directx/downloads/default.asp](http://www.microsoft.com/windows/directx/downloads/default.asp)

DirectX is a registered trademark of Microsoft Corporation.

# 4) Main Screen

```
Fig 1: Main Screen of FFShifter.
```

4.1) Start Button

Starts the initialization of the FF Joystick and polls the joystick at a predefined rate
(configurable). If it is the first time running the program, you are advised to choose
which joystick you want to use from the config screen. When Start is pressed, the only
buttons enabled are the checkboxes, the stop and quit buttons.

4.2) Start With Delay Button

Same as the Start Button but FFShifter waits for a specified amount of time (from the
config screen), before it initializes the joystick. This option is to be used for games
like Richard’s Burns Rally that do not allow the hot key to turn on FFShifter.

4.3) Stop Button

Stops the polling of the joystick, and the Config and About buttons are enabled.

4.4) Info Area

In this area you get in which mode is FFShifter (H-Pattern or Sequential) and which
forcefields file is loaded..

4.5) Draw Options

Here you can control what you see on the white display area.
The Draw checkbox turns on/off of all graphics.
The Draw Shifter Gates checkbox turns on/off the drawing of the sifter gates (the red
H shape). The original purpose of the shifter gate shape was to provide collision data
for the joystick, but since it proved impossible, they are only there for illustration
purposes.
The Draw ForceFields checkbox turns on/off drawing of forcefields. Forcefields are
areas, that activate a force when the joystick cursor is in them.
The Draw Constant Forces checkbox turns on/off the drawing of constant force
forcefields (in blue). Constant forces forcefields are areas that actually lock the
joystick into a gear, and they have a key associated with them, which is sent to the
racing sim. If this key is configured in the racing sim as an actual gear, you will get a
gear shift.
The Draw Spring Forces checkbox turns on/off the drawing of spring forcefields (in
green). Spring forcefields are areas that activate spring forces on the joystick, so when
it is unlocked from a gear, if left free, it will return to center (neutral position).

4.6) Config Button

The Config button opens up the configuration screen.

4.7) Quit Button

The Quit button exits the program.


# 5) Configuration Screen

```
Fig 2: The Configuration Screen
```
5.1) Select FF Joystick

In this combo box you will find all the FF devices detected on your system. Select
which one is your joystick which you will use as a gear shifter.

5.2) Joystick Button for Reverse

You select the joystick button that will activate the secondary key press of a forcefield
(if that is specified). Its use is mostly for a forcefield that has been defined with a
primary key press for a gear and a secondary key press for a reverse gear.


5.3) Select ForceFields File

When you press select you get the following screen:

```
Fig 3: Selecting a forcefield file
```
Inside the combo box you will find all the available forcefields definition files (with
extension .fff), which are located in the “forcefields\” folder. With the current release
you get 4 files:

Simple_6_gears_R.fff : 6 gear positions (1:w, 2:s, 3:e, 4:d, 5:r, 6:g) and if you shift
into 1st gear with the specified reverse button of your joystick you will activate the
reverse gear (R:q).


Simple_5_gears_R : 6 gear positions (R:q,1:w, 2:s, 3:e, 4:d, 5:r).

The two simple forcefield files, have been designed for users of the Logitech
Wingman Force (the old version of the Logitech Wingman Force 3D). As it seems
this old joystick allows only 8 forces to be downloaded into memory, so these two
files do not use more than 8 forces.

6_gears_R : Same number of gears as the simple one, but it uses more springs to
stabilize shifts (although the simple forcefields are quite stable as well).

5_gears_R : Same number of gears as the simple one, but with more springs to
stabilize shifts.

These forcefields are mere examples of what you can design with the force editor.


5.3) Select Plate File

Likewise, with the select button you can select a gear shifting plate located in the
“plate\\” folder (with extension .ase). As already stated a plate file is used only for
illustration purposes and has no effect on FFShifter.

5.4) Other Options

5.4.1) Enable Error Logging

When selected, FFShifter writes certain events and errors in a log file called
FFShifter.log. Also you will find an executable of FFShifter called
“FFShifterDebug.exe”. If you happen to have problems with FFShifter (likes crashes),
run “FFShifterDebug.exe”, enable error logging and try to replicate the problem. Then
email the error log file at ffshifter@gmail.com for reviewing and a possible bug fix.

5.5) Sequential Shifting Mode

Some racing sims do not provide control options to specify individual key pressed for
each gear, and they only support two buttons, one for shifting up and one for shifting
down. FFShifter supports sequential shifting mode by calculating how many key
presses are needed to go from one gear to another.

5.5.1) Sequential Mode

When selected, FFShifter calculates the necessary key presses, and emulates a
sequential shifter, although you may be still using an H-pattern shifter. This option
allows the use of FFShifter in older games, that only allowed two buttons for shifting.

5.5.2) Sequential Shift Up Key

You select which key will be sent for shifting up. When in sequential mode, FFShifter
is not sending the key presses defined in the forcefields file, but is sending the keys
specified here.

5.5.3) Sequential Shift Down Key

Same as in 5.5.2 but for shifting down.

5.5.4) Joystick Button for Reset

If you are using an H-pattern forcefield, FFShifter calculates the number of key
presses needed to shift from one gear to another and remembers the current state. If
you happen to crash and the car starts in neutral and FFShifter remembers that is in
another gear, they will be out of sync. So you can define a joystick button for resetting
FFShifter back to neutral (only in sequential mode).

5.6) Draw Options

Same as in section 4.5.


5.7) Sound Options

Here you can enable sound effect playback, or turn on/off specific sound effects.

5.8) Timing

5.8.1) Joystick Poll Thread Priority

You can set the priority of the thread that polls the joystick for information. If you
find that FFShifter is using too much CPU, you can lower the thread priority.

5.8.2) Joystick Poll Rate

This is the rate that the program is polling the joystick in milliseconds. If you find that
FFShifter is using too much CPU time, you can try a slower poll rate (like 20 or 30
ms).

5.8.3) GearShift Delay

When a gear shift is activated there is a small delay before the program continues to
poll the joystick. If you want faster gear shifts, you can even set it to zero.

5.8.4) Sequential Key Press Delay

When is sequential mode, FFShifter sends two keyboard events, one for key press
down and one for key press up. In between these two events there is the need of a
small pause, so that the game can detect the event. If you find that a game is not
picking up key presses while in sequential mode (or that it loses some of them) try
setting the delay time a bit higher.


# 6) Force Editor

By pressing the Editor button from the main screen, you activate the Force Editor (Fig
4), where you can edit the existing forcefield files or you can create your own.

```
Fig 4: The Force Editor dialog.
```
```
Fig 5: The forcefield file selection combo.
```
In Fig 5 you can see the forcefields file selection combo box. Here you can select
which forcefield you want to edit.
In case you want to create a new one, you press the Create button, enter a new name,
and a new empty forcefields file will be created.
If you want to delete an existing forcefields file, you can press the Delete button, and
after confirmation you will delete forever the selected forcefields file.


```
Fig 6: The forcefields contained in a forcefield are displayed in a list box.
```
In Fig 6 you can see the list box, where all the forcefields contained in a forcefield file
are listed.
By pressing the Add button you can add a new forcefield (the relevant fields – Fig 7,
are enabled).

```
Fig 7: The fields of a forcefield.
```
Common Fields

- Name : You can assign a name to the forcefield.
- Shape : Currently the only shape available is the rectangle.


- Pos X & Pos Y : The coordinates of the center of the forcefield. When you
    add a new forcefield, its center is located at the joystick cursor (the red circle
    with the cross).
- Width & Height : The width and height dimensions of the forcefield.
- Type of Force : The type of forcefield; there are two types of forcefields, a
    constant force forcefield, which applies a constant force to the shifter towards
    a specific angle, and a spring force which emulates the force of a spring acting
    upon the shifter. When you are creating a new forcefield, this is the first field
    you should modify, to select the type of force you desire (every time you
    change it, the forcefield is reset to its default values and position).

Constant Force Fields

- Auto Calculate Force Angle : If checked, when you move the forcefield
    in the editor, its angle is calculated and updated automatically.
- Force Angle : You can enter a value between 0-359 degrees (Fig 8).

```
Fig 8: The force angle directions
```
- Force Min Power : This is the minimum force power (-100 to 100) of the
    constant force (it will be used in a future release as the power applied when the
    clutch is pressed). Currently it is not being used.
- Force Max Power : This is the maximum force power (-100 to 100) of the
    constant force. When negative, it has the opposite direction of the force angle.
    This value is the one currently being used.

Spring Force Fields

- Force Power X : The spring force in the X axis (-100 to 100). A negative
    value, signifies an opposite direction in the X axis from the offset point.
- Force Power Y : The spring force in the Y axis (-100 to 100). A negative
    value, signifies an opposite direction in the Y axis from the offset point.
- Offset X & Offset Y : The XY coordinates of the spring’s offset point.
    The offset point is simply the resting point, at which the spring is at a
    balance. The coordinates can range from -1.0 to 1.0.


Key/Sequential Gear Values

- Primary Send Key : When you want a forcefield to send a key press select it
    from the Primary Send Key combo box.
- Secondary Send Key : A forcefield can send an alternative key press, when it
    is activated while pressing the joystick button defined in the config screen as
    Joystick Button for Reverse (5.2). This way you can define a forcefield to act
    as two gears. For example you can define a 1st gear forcefield to send the key
    W and when the same forcefield is activated with the Reverse Button
    depressed, it can send the key Q as a Reverse Gear.
- Primary Sequential Gear Value : If you want to use the forcefields file in
    sequential mode as well, you must define the sequential gear value for a
    forcefield that acts as a gear. So you would assign 0 for R, 2 for 1st gear, 3 for
    2 nd gear and so on...
- Secondary Sequential Gear Value : If you have assigned a secondary send
    key, you will need to assign a secondary sequential gear value as well.

```
When adding or editing forcefields, changes are not saved until you press the Save
Button. The Cancel button will discard changes. When you are adding a new
forcefield, you can only edit this new forcefield. But when you are editing you can
edit all the forcefields and the changes will be saved only when you press the Save
button.
```
The Activate Joystick button, initializes the selected joystick from the config screen,
and you can see it’s cursor in the Force Editor Graphics Window. If you have
activated the joystick, and you are not adding or editing a forcefield, you can also
activate the forcefields to test them out.

```
Fig 9: All forcefields are activated for testing.
```

When all forcefield are activated (Fig 9), they are all highlighted and all the other
fields are disabled. You must deactivate the forcefields, for all the fields to be enabled
again (or deactivate the joystick which will also deactivate the forcefields).

Mouse X & Mouse Y display the mouse coordinates when the mouse cursor is the
graphics window. Finally the Close button, exits from the Force Editor.

6.1) Interactive Manipulation of Forces in Graphics Window

```
Fig 10: A constant force forcefield.
```
In Fig 10 we can see how a constant force forcefield appears in the graphics window.
When adding or editing a constant force forcefield, we can use the mouse over the
square points to manipulate its attributes. The four squares on the sides of the
rectangle can be used to alter the width and height of the rectangle.
The grey line represents the force angle, and by dragging the grey square on the edge
we can determine the force angle. The orange line represents the maximum force
power and the black line the minimum force power (again dragging the squares will
change the respective values). If the mouse is over the forcefield and not over of any
of the squares, by dragging we can change the position of the forcefield.

```
Fig 11: A spring force forcefield.
```
In Fig 11 we can see how a spring force forcefield appears in the graphics window.
When adding or editing a spring force forcefield, we can use the mouse over the
square points to manipulate its attributes. The four squares on the sides of the
rectangle can be used to alter the width and height of the rectangle.
The orange line represents the offset point of the spring. You can thing of the offset
point, as the point towards the spring pushes the shifter. Whenever you move the
offset point by dragging with the mouse the orange square point, you will see the
black lines that represent the spring’s X and Y forces to change direction. This


happens because a spring axis force when it has a positive value, it points towards the
offset point and when it has a negative value it points away from the offset point.
In a similar way, by dragging the black squares you can modify the X (horizontal) and
Y (vertical) force values. If the mouse is over the forcefield and not over of any of the
squares, by dragging we can change the position of the forcefield.

When editing a forcefield file (edit is pressed), you can select a different forcefield
rectangle for editing (without the need of continuously pressing the Save button)
either by selecting from the forcefields list box (Fig 6), or by holding down the Ctrl
button and left clicking with the mouse over the desired forcefield. Bare in mind
though, that all changes to all forcefields, won’t be applied until you press the Save
button.

# 7) Beta Testing

If you find any problems with FFShifter please email a description of the problem at
ffshifter@gmail.com along with an error log file, a detailed description of reproducing
the problem and a hardware specification like this:

CPU Intel P4 3000 MHz
RAM 1 GB
OS WinXP SP
DirectX DirectX 9.0 c
Joystick Logitech Wingman Force 3D
Wheel Logitech MOMO (black)
Game LFS. GTR
