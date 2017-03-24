
Odour Delivery Module (ODM) 
=========================
The Odour Delivery Module (ODM) is an Ethoscope module that allows us to delivery up to two different olfactory stimuli to fruit flies held in 14mm glass tubes. 
Odour can be delivered in response to fruitfly behaviour. For instance, following an immobility bout or  a crossing of a virtual midline. 

The ODM can be configured in two different ways; **single** or **dual** odour delivery. 
The frame for dual odour delivery can house two splitters, whereas the frame for single odour delivery houses just one. 
As the former frame is slightly larger, the 3D printed platforms which support the Ethoscope, are slightly different sizes. 
Gcode files for two different versions of the 3D printed frame and platform are available upon request.  
Assembly of the 2 versions of the modules is otherwise similar. 
The assembled odour delivery module with Ethoscope looks like this (this is an example of a a single odour delivery module):

Figure 1 Ethoscope + ODM

A list of components (BOM) for the ODM is available [here](BOM.csv).
In this document we describe how to build the ODM. 
Before we start, this image shows components needed. 
[Pic with all components]
Circuitry
* Cut USB cable 30mm from micro port.  Strip black cable and separate red and black wires inside main cable. Strip black and red cables by approximately 5mm and use micro screwdriver to secure **black cable into VS1-** and the **red into VS1+** on region of lynx motion board labeled 1. 
* Plug in mini port of 2nd USB cable [2].
* Plug in power supply to Anker 40w PSU and USB cable into USB port of computer. **Press the button labeled 3 until green and red lights (labeled 4) are both on and not flashing**. Use a piece of blue tac to cover the lights so they do not disturb the flies during an experiment.
* Place the lynx motion in the base of the frame so that the pins labeled VS1 are in the center.  
* Self-adhesive cable clips can be used to secure the cables and lynx motion into the bottom of the frame (not shown). This can prevent the power supply disconnecting from the lynx motion.

Figure 2 Preparation of Lynx motion
* Next, take the using the 2x10mm screws, secure the 10 x 9G servo motors to the frame of the 2 3D printed shelves (2 screws per servo). 
* Plug the cables of the servo motors into the lynx motion board (Figure 3). The brown cable should correspond to the pin on the outer edge of the VS1 row of pins. The servos should be plugged in the following order:
Servo number
Pin label on lynx motion
1 (shelf 1)
0
2 (shelf 2)
1
3 (shelf 1)
2
4 (shelf 2)
3
5 (shelf 1)
4
6 (shelf 2)
5
7 (shelf 1)
6
8 (shelf 2)
7
9 (shelf 1)
8
10 (shelf 2)
9

* Run script ‘zero_all_servos.py’ to zero all the servos [Q can you update here with link to python script for this part]. 
* Using the 2x6mm screws, screw the cog onto the servos (shortest straight edge of cog should be closest to base of shelf and exactly parallel), whilst they are being locked at 0 position. Make sure that the cogs are tightly secured (these can be printed at 101% to make extremely tight).  
* Insert the Lego Technic Pins. Screw into place using the 2x6mm screws (optional).
 
Figure 3 Servo configuration

Modifying Lego Pneumatic valves
Some of the pneumatic valves are quite stiff and need to be modified; otherwise we find the servos burn out quickly whilst changing lever position during experiments. Please use cut proof gloves and eye protection for this part.
You will need a vice, Stanley knife (with sharp blade), super glue and dust cleaner spray can.
-Place lego pneumatic valve in vice with back edge facing towards you. Using the Stanley knife slice down the grooves between the back panel and valve case. Rotate the valve in vice and cut along the grooves until the glue sticking 3 edges of the back panel to the valve case, is broken.
[Insert pic]
-The back panel is also glued inside the valve to a plastic rod. The dimple in the back of the valve back panel indicates the point of adhesion, so once the back panel is loosened; you will need to slip the knife inside the valve and slice along the back panel to break this glue. To remove the back panel fully you will also need to cut inside parallel to the back panel at two top corners of the valve (see figure?)

[insert pic with cut lines]

- Once the back panel is removed, carefully remove the black lever mechanism. Place somewhere it will not get dusty. It is coated with an oil based lubricant, so be careful not to remove this. 
-Next you will need to remove two small nodules on the inside edge of the valve base. This will allow the black lever mechanism to move more freely from side to side. Do this using the Stanley knife. 
-Clean any shards of plastic from the inside of valve using the dust cleaner spray. Replace the black lever mechanism and stick the back panel back on using a small amount of superglue on each corner. 
-Place in clamp and allow to dry.
-Test valve is working properly and the lever moves freely following this modification. 
Final Steps of Assembly
-Place the 3D printed lever onto the black lever mechanism of the valve (rounded edge down).
- With correct alignment, the two holes in the base of the lego valve should slide onto the lego technic pins (already screwed onto shelves), and the 3D printed lever should slide into the square hole on the 3D printed cog attached to the servo. The lego pneumatic valve should click into place as there is a small lip on the edge of the lego technic pins.
- Next take 1 or 2 fish tank splitters (depending on frame being used) and using a Stanley knife, shorten the length of the input by 15mm. Attach the 10mm OD silicone tubing to the input. Place the 10 or 20 (depending on configuration) 5mmOD12mm lengths of silicone tubing on each of the splitters output. 
[image]
-Thread the 10mm OD silicone tubing through the hole(s) in the 3D printed frame (from inside to out) and slot the fish tank splitter(s) into the groove(s) in the frame. 
-Using the 2x10mm screws, screw the shelves onto the frame,(lego valves facing outwards and servo backs inside). Use sandwich bag wires to tie the servo cables and tuck under the shelves. 
* make sure that servo 1 is to the front left hand side of the ODM Servo 10 should be back right hand corner  (when the hole(s) for the 10mmOD tubing is facing you).
- For single odour delivery, attach the 5mmOD silicone tubing (which is attached to splitter to the lower port of each valve (Figure 4).

Figure 4 Single odour delivery
-For dual odour delivery, attach all 5mmOD silicone tubing originating from one splitter to the upper left port and all of the 5mmOD silicone tubing originating from the second to the upper right port (Figure 5). 

Figure 5 Dual odour delivery
- Using 2x6mm screws attach 3D printed platform to top of frame. There are two Gcode versions of this platform depending on whether you are using frame designed to hold 1 or 2 fish tank splitters (Figure 6). The Ethoscope sits on top of the ODM. Flies within the glass tubing (L,OD,ID: 140mm, 5mm, 3mm) in the Ethoscope arena are connected to the odour supply via 5mm (OD) silicone tubing connecting to the left upper port (for single odour delivery) and the bottom middle port (for dual odour delivery). The USB cable from ODM connects to Ethoscope USB port. Both Ethoscope and ODM connect to power supply. 

Figure 6 ODM with platform
