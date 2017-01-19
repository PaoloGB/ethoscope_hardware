
Optomotor Module
=========================


The optomotor is an ethoscope module that allows us to deliver both mechanical (tube rotation) and optical (LED) stimuli to fruit flies.

The assembled module will look like this:


[[pictures A (module), B module+ ethoscope]]


Conceptually, the module contains three distinct parts:

* "main", the mandatory components

* "opto", only needed for optical stimulus delivery

* "motor", only needed to rotate tubes


A list of components (BOM), and their respective part is available [here](BOM.csv).

In this document, we describe how to build both opto and motor parts.

Therefore, before we start, we have something like this:


[[picture overview]]


Main
-----------------------------------------------

The idea is to prepare two electronic boards : Arduino micro and TLC5943, screw them to the bottom of the main box and connect them to each other. Also, we add a push button for testing purposes.

###Trimming the main box

The main box is a large print with a lot of support, and it is easier to trim it before putting anything sensitive inside.


### Arduino board

This is the "master" board that processes input from the computer and coordinate the stimulus delivery.

 1. Solder a 4-pin header (cut a 6-pin header two, 4+2) between pins 3 and 6 (see picture below)

 2. Solder a 2-pin header between pins 11 and 12

 3. Screw the board in place using the 1.2mm diameter screws.

 4. Plug the USB micro cable to the board. Then compile and upload the firmware (you need some degree of familiarity with the arduino [build process](https://www.arduino.cc/en/Hacking/BuildProcess) for that). The code for this firmware lives [here](https://github.com/gilestrolab/ethoscope_hardware/blob/master/modules/optomotor/optomotor.ino).


So, at this stage, we have:


[[picture arduino board]]


### TLC5943

This board is the "slave". It is ultimately responsible of turning on/off components (LED/motors).


1. Solder all (i.e. 8) the 6x2 headers (see picture below)

2. Solder the 2 6x1 headers on both extremities of the board

3. Solder the 1.15kΩ resistor

4. Screw the board in place -- using the 2.6mm diameter screws


So now we have both boards in:


[[picture both boards]]


#### Board connector

The connections between the two above boards has to be very robust at all time.

To build the connector (picture below), we use **80mm** of **6-way** ribbon cable. Four of the wires connect the two boards, whilst 2 bring external power to the TLC5943.


1. Strip all six wires on one end.

2. Squeeze each wire on a different slot of female connector

3. Solder all six wires (this is a bit of a hack, but it works well if you don't have the tool for these connectors)

4. Cut the two wires on the right so that the are only **20mm** long

5. Solder the four remaining wires to the second female connector (the wire must obviously have the same order and position on the second connector -- e.g. in the picture, yellow is on the left of both connectors)

6. Add a 2-pin socket (using two crimps connectors) to the two short remaining wires


The connector itself looks like this:


[[picture connector]]


When connecting the tow board, we want the pin named "LAT" on the TLC5943 to connect to pin 6 on the arduino (yellow cable),


[[picture connected boards]]


### Push button


To assemble the push button:


1. cut a **150mm**, **3-way** (green, black, white) ribbon cable (picture below)

2. Strip the three ends, and preload some heat shrink before you solder

3. Solder the V+ (white) cable directly to a pin of the push button (it doesn't matter which one)

4. Solder the digital out (green) pin directly to the other pin

5. Solder the ground (black) to the same pin as the digital out, but **through the 1.15kΩ resistor**

6. Figure out the heatshrink issue (good luck)

7. Cut the ground and V+ wires to **80mm**

8. Use crimps connectors to put ground and V+ in the same 2-pin female socket

9. Use crimps connector to put the digital out wire on a 2-pin female connector (one of the slot will be empty, but do put a crimps connector inside anyway. This makes a better mating between connectors)

10. Bundle all the wires/resistor on the push button end with some larger heat shrink or electrical tape

11. Pass the assembled psh button from the inside of the box to the outside inside the small hexagonal cavity, and lock it using the hexagonal screw from the outside. Admittedly, it is not very to spin the push button at this stage, but it will work with some determination!

12. Connect the V+ and ground pins to the corresponding pins on the **TLC5943** board

13. Connect the digital out wire on **pin 12** of the arduino


[[picture assembled push button]]


So In the end, the assembles and connected push button looks like this:


[[picture connected push button]]

Opto
------------------

In order to deliver light to specific tubes, we will make an array of LEDs and connect the LED, with optic fibres, to individual tubes.

Each LED is fitted inside a panel, their are two panels (left and right), each holding 5 LEDs per machine. The panels are held in position by the "clips"


1. Trim the clips and panels (2 of each), so they fit without forcing. Also remove any support structure on the LED panels.

2. Set the LEDs so that the + side is on the left (see picture)

3. cut all the LED legs to 3mm or so

4. Prepare (strip bot ends) as many **75mm**, **2-way** ribbon cables

5. Put a 2-way female socket on one end (using the crimps connectors)

6. Put some heat shrink (5mm should do) on each wire on the other side of the cable.

7. Solder the LEDs. In this document, by **convention**, we use **violet for - ** and **light grey for +**

8. Process the heat shrinks


To summarise, this is something like that:

[[picture LED panel]]


Motor
--------------------

Motors each have their own individual slots, so we can just make 10 motors and fit them on the box.


1. Prepare (strip bot ends) as many **150mm**, **2-way** ribbon cables

2. Put a 2-way female socket on one end (using the crimps connectors)

3. Put some heat shrink (5mm should do) on each wire on the other side of the cable.

4. Solder the motors. In this document, by **convention**, we use **green for - ** and **blue for +**. The Motors have a little "+" written by the corresponding pole.

5. Pass each motors through their slot in the main box

6. Put its shaft (3d printed small orange part) to each motor

7. add a ring of silicon (i.e. a section of tube around **5mm long**) to each shaft -- this ensure maximal friction



An assembled motor looks like this:


[[picture assembled motor ]]


Then, when mounted, they look like that:


[[picture mounted motors]]

Putting things together
-------------------------------------

In the end, we need to assemble the whole thing.



[[todo!!]]

