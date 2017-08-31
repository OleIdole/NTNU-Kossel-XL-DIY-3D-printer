Legg inn bilde med skalering: <a href="url"><img src="link" align="center" height="400" width="400" ></a> <br>

# Step-by-step guide to building your own 3D-printer

## Part list
 Part | Quantity 
----- | -----
M4x12mm screw | x
M3x20mm screw | x
M3x12mm screw | x
M3x8mm screw | x
M3 nut | x
T-nut | x
Compression spring 5mm | x
Cork 3mm | x
Cork 1.5mm | x


## Preparation of parts

### Step 1 - Tie rod carbon tubes
<a href="url"><img src="https://github.com/OleIdole/Kossel-XL-DIY-3D-printer/blob/master/Pictures/Carbon%20rod.jpg" align="center" height="403" width="302" ></a> <br>
Apply glue to the tie rod end and insert it into the tie rod carbon tube. **Avoid applying glue to the bearing.**<br>
Loctite Power Epoxy Universal works well for this, but other types can also work.<br>
**Make sure that the tie rod ends does not slide out while the glue dries.**<br>
**Make sure that the tie rod ends on both sides are equally rotated.**<br>

### Step 2 - Carriage
<a href="url"><img src="https://github.com/OleIdole/Kossel-XL-DIY-3D-printer/blob/master/Pictures/Carriage%20on%20rail.jpg" align="center" height="403" width="302" ></a> <br>
**Make sure the carriage does not slide off the linear rail, there are loose parts inside!**<br>
Assemble the carriage similar to the picture. These will later be used to keep the belt tightened and also move the delta arms.<br>
The 2 screws at the top are 20mm M3 that need to be cut down a few mm. The screw at the bottom is a 10mm M3 screw.<br>
The screw used to keep together the 3D-printed parts is 20mm M3 with a M3 nut.<br>
All the screws that attach to the carriage should be inserted once before assembly to break the grooves in the PLA. This will allow the parts to be assembled tighter.<br>
Cut down 2x 20mm M3 screws about 4mm down. Now insert 2x M3 nuts into their slots in the 3D-printed part.<br>
Insert the screws from the side of the carriage until they attach to the nuts. These will be used for the carbon rods later.<br>


### Step 3 - Ramps 1.4 jumper settings
<a href="url"><img src="https://github.com/OleIdole/Kossel-XL-DIY-3D-printer/blob/master/Pictures/Ramps%20stepper%20jumper%20settings.jpg" align="center" height="403" width="302" ></a> <br>
There are 3 jumper settings for each stepper.
The jumpers settings for each step size is listed below:

jumper1 | jumper2 | jumper 3 | step size
------------ | ------------- | ------------- | -------------
 no  |  no |   no |  full step
 yes |  no |   no |   half step
 no  |  yes |   no |   1/4 step
 yes |  yes |   no |   1/8 step
 no  |  no |   yes |   1/16 step
 yes |  no |   yes |   1/32 step
 no  |  yes |   yes |   1/64 step
 yes |  yes |   yes |   1/128 step
 
If the jumpers are set to a higher number of micro steps than supported by the driver, it will operate at the maximum possible number of micro steps for that driver. Because of this, **we will set jumpers on all 3 settings** which means 1/128 is the maximum step size.<br>
Since we use the pololu  A4988 stepper motor drivers, this results in 1/16 micro stepping.<br>
**We will use the same settings for all steppers (X,Y,Z,E0,E1).**<br>
<br>
<a href="url"><img src="https://github.com/OleIdole/Kossel-XL-DIY-3D-printer/blob/master/Pictures/Stepper%20drivers.jpg" align="center" height="302" width="403" ></a>  <a href="url"><img src="https://github.com/OleIdole/Kossel-XL-DIY-3D-printer/blob/master/Pictures/Drivers%20on%20ramps.jpg" align="center" height="403" width="302" ></a> <br>
Now find the stepper drivers, place the heat sink on top of these.<br>
**Make sure the heat sink doesnt touch any electrical circuits!**<br>
Insert the drivers on top of the ramps 1.4 as in the picture above.<br>
Underneath the driver you will see where each pin belongs. This makes it simple to see which way it should be placed onto the ramps card.<br>
<br>
Now place the ramps 1.4 on top of the arduino card. Make sure none of the pins are bent, then press push it together.<br>


### Step 4 - Power supply
<a href="url"><img src="https://github.com/OleIdole/Kossel-XL-DIY-3D-printer/blob/master/Pictures/Power%20supply%20voltage%20switch%201.jpg" align="center" height="403" width="302" ></a>
<a href="url"><img src="https://github.com/OleIdole/Kossel-XL-DIY-3D-printer/blob/master/Pictures/Power%20supply%20voltage%20switch%202.jpg" align="center" height="403" width="302" ></a> <br>
It is important to change the voltage setting of the power supply before it is used.<br>
Since we operate with 230V we have to flip the switch from 115V to 230V on the side of the power supply.<br>
<br>
Attach the 3D-printed brackets onto the power supply. Do not attach the relay yet.<br>
When finished, it should look like the images below.<br>
<a href="url"><img src="https://github.com/OleIdole/Kossel-XL-DIY-3D-printer/blob/master/Pictures/Power%20supply%20brackets%201.jpg" align="center" height="302" width="403" ></a>  <a href="url"><img src="https://github.com/OleIdole/Kossel-XL-DIY-3D-printer/blob/master/Pictures/Power%20supply%20brackets%202.jpg" align="center" height="403" width="302" ></a> <br>


### Step 5 - Top corner bearings
<a href="url"><img src="https://github.com/OleIdole/Kossel-XL-DIY-3D-printer/blob/master/Pictures/Bearings%20top%20set.jpg" align="center" height="302" width="403" > </a><a href="url"><img src="https://github.com/OleIdole/Kossel-XL-DIY-3D-printer/blob/master/Pictures/Bearings%20assembly%20order.jpg" align="center" height="403" width="302" ></a> <br>
The pictures above show an overview of how the assembly order will be. The screw will first go through the hole of the corner, so dont assemble it just yet.<br>
<a href="url"><img src="https://github.com/OleIdole/Kossel-XL-DIY-3D-printer/blob/master/Pictures/Bearings%20top%20corner.jpg" align="center" height="403" width="302" ></a> <br>
Assemble the corners similar to the picture above.<br>
The order for the screw is: through first hole > washer > both bearings > washer > nut. Tighten the screw.<br>
It is recommended to use pliers to keep the nut in place as instructed in the picture below.
<a href="url"><img src="https://github.com/OleIdole/Kossel-XL-DIY-3D-printer/blob/master/Pictures/Bearings%20use%20pliers.jpg" align="center" height="400" width="400" ></a> <br>


### Step 6 - Attach tooth pulley to stepper motors
<a href="url"><img src="https://github.com/OleIdole/Kossel-XL-DIY-3D-printer/blob/master/Pictures/Tooth%20pulley%20stepper%20motors.jpg" align="center" height="403" width="302" ></a> <br>
Attach the tooth pulley to the stepper motor as this will not be possible after motor is assembled to the corner.<br>
Position the tooth pulley similar to the picture above, make sure there is a slight gap between the motor and the tooth pulley to prevent friction.<br>
Tighten the 2 screws on the tooth pulley with 1 of them facing the flat part of the rod.<br>


### Step 7 - Insert nuts into the 3D-printed T-nuts
<a href="url"><img src="https://github.com/OleIdole/Kossel-XL-DIY-3D-printer/blob/master/Pictures/Printed%20%20Tnuts.jpg" align="center" height="403" width="302" ></a> <br>
Insert M3 nuts into the 3D-printed T-nuts like in the picture above.<br>
Apply light pressure with a hammer until the nuts are flush with the T-nut.<br>

### Step 8 - Assemble hotbed mount
<a href="url"><img src="https://github.com/OleIdole/Kossel-XL-DIY-3D-printer/blob/master/Pictures/Hotbed%20mount%20assembly.jpg" align="center" height="302" width="403" ></a> <br>
Cut the 5mm diameter spring into a length of approximately 5 full revolutions.<br>
Place M3 nuts inside the regulator as in the picture above.<br>
Insert 20mm M3 screws and position it similar to the picture, these will be adjusted when calibrating.<br>
<br>
<a href="url"><img src="https://github.com/OleIdole/Kossel-XL-DIY-3D-printer/blob/master/Pictures/Cork%20hotbed%20frame.jpg" align="center" height="302" width="403" ></a> <br>
Apply cork to the hotbed mount. One layer to the adjustable part, one to the static part and one to each side.<br>
When finished it should look like the picture above.<br>


### Step 9 - Assemble fan holder
<a href="url"><img src="https://github.com/OleIdole/Kossel-XL-DIY-3D-printer/blob/master/Pictures/Solder%20power%20switch%201.jpg" align="center" height="403" width="302" ></a>  <a href="url"><img src="https://github.com/OleIdole/Kossel-XL-DIY-3D-printer/blob/master/Pictures/External%20power%20cable.jpg" align="center" height="302" width="403" ></a> <br>
First you need to do some soldering. Cut the external power cable close to the end where the plug is.<br>
You want to access the wires as the plug will not be used. Strip open about 6cm of the isolation, which should be enough for soldering, if not, take some more.<br>
Insert the external power cable through its appropriate hole, then out where the switch belongs. This way you can drag it back when you are finished soldering.<br>
**Use heatshrink tubes on all soldering points to ensure optimal insulation.**<br>
Insert heatshrink tubes onto the cables.<br>
Solder the brown wire onto one of the pins of the on/off power switch.<br>
Cut about 30cm of 1.5mm2 black wire and solder onto the other pin of the switch.<br>
Cut about 30cm of 1.5mm2 red wire and solder onto the blue wire from the external power cable.<br>
Cut about 30cm of 1.5mm2 yellow/green wire and solder onto the yellow/green wire from the external power cable.<br>
Apply heat to the heatshrink tubes until appropriately shrinked. Now place the switch into its slot.<br>
Apply a cable tie to the external power cable at the inside of the fan holder to prevent it from being pulled out.<br>
Now it should look like the pictures below.<br>
<a href="url"><img src="https://github.com/OleIdole/Kossel-XL-DIY-3D-printer/blob/master/Pictures/Solder%20power%20switch%202.jpg" align="center" height="403" width="302" ></a>  <a href="url"><img src="https://github.com/OleIdole/Kossel-XL-DIY-3D-printer/blob/master/Pictures/fanholder%202.jpg" align="center" height="403" width="302" ></a> <br>
<br>
<a href="url"><img src="https://github.com/OleIdole/Kossel-XL-DIY-3D-printer/blob/master/Pictures/Fans%20for%20fan%20holder.jpg" align="center" height="302" width="403" ></a> <br>
Insert 2 fans as in the picture above, pull the wires out of its slot, so they hang loose on the inside.<br>
You only need to use 2 screws for each of them.


### Step 10 - Solder end stops
<a href="url"><img src="https://github.com/OleIdole/Kossel-XL-DIY-3D-printer/blob/master/Pictures/Solder%20end%20stops.jpg" align="center" height="403" width="302" ></a>  <a href="url"><img src="https://github.com/OleIdole/Kossel-XL-DIY-3D-printer/blob/master/Pictures/Twisted%20wires.jpg" align="center" height="403" width="302" ></a> <br>
Cut 0.5mm2 wires of about 1.5m length. Wires can probably be of much shorter length, this is just to avoid them being too short.<br>
If you dont have 0.5mm2 wires, use bigger ones.<br>
Attach the wires to a drill, and the other end to a vice or something similar to hold it.<br>
Now drill it until the wires are twisted together similar to the picture above.<br>
Apply heat shrink tubes and solder the wires onto the end stops.<br>


### Step 11 - Assemble hotend
The hotend should be assembled according to E3D's official tutorial, [click here for the tutorial.](https://wiki.e3d-online.com/wiki/E3D-v6_Assembly)<br>


## Assembly

### Step 1 - Insert T-nuts into the short 20x20 profiles
<a href="url"><img src="https://github.com/OleIdole/Kossel-XL-DIY-3D-printer/blob/master/Pictures/T-nut.jpg" align="center" height="403" width="302"></a> <br>
**This part is for the profiles on the bottom section, not the top part of the printer**<br>
Insert T-nuts into the 20x20 profiles according to the list below:<br>
<br>
**Front:**<br>
Lower inside : 6<br>
Upper inside : 6<br>
<br>
**Left side:**<br>
Lower inside : 5<br>
Upper inside : 5<br>
<br>
**Right side:**<br>
Lower inside : 4<br>
Upper inside : 6<br>
<br>

#### Dette skal lenger ned i guiden, beholder her midlertidig.
Inside of all towers (the long 20x20 profiles):<br>
lowest 1 x m4, in the midle 7 x m3 and on topp 1 x m4 <br>
Depends on the carry profile that is used. We used one with 24xm3 holes. <br>
And we used m4 for the end brackets. (lower and upper) <br>


### Step 2 - Attach stepper motors
<a href="url"><img src="https://github.com/OleIdole/Kossel-XL-DIY-3D-printer/blob/master/Pictures/Stepper%20motor.jpg" align="center" height="403" width="302" ></a> <br>
Place the stepper motor inside the corner and tighten all 4 screws. This can be tricky due to minimal workspace, using pliers might help. Make sure the wires face down.<br>
Also its worth noting that cutting an umbraco for this part will make life much easier, shown below.<br>
<a href="url"><img src="https://github.com/OleIdole/Kossel-XL-DIY-3D-printer/blob/master/Pictures/Cut%20umbraco%20for%20M3%20screws.jpg" align="center" height="403" width="302" ></a> <br>


### Step 3 - Assemble bottom frame
<a href="url"><img src="https://github.com/OleIdole/Kossel-XL-DIY-3D-printer/blob/master/Pictures/Bottom%20frame.jpg" align="center" height="403" width="302" ></a> <br>
Assemble the corners together with the small 20x20 profiles similar to the picture above.<br>


### Step 4 - Assemble top frame
<a href="url"><img src="https://github.com/OleIdole/Kossel-XL-DIY-3D-printer/blob/master/Pictures/Top%20frame.jpg" align="center" height="403" width="302" ></a> <br>
Insert 4 T-nuts on the inside of each small 20x20 profile.<br>
Assemble the corners together with the small 20x20 profiles similar to the picture above.<br>


### Step 5 - Attach linear rails and end stop brackets
**Make sure the carriage does not slide off the linear rail, there are loose parts inside!**<br>
<a href="url"><img src="https://github.com/OleIdole/Kossel-XL-DIY-3D-printer/blob/master/Pictures/Linear%20rail.jpg" align="center" height="403" width="302" ></a> <br>
Assemble the linear rail to the long 20x20 profile using the 3D-printed T-nuts.<br>
Do not tighten this yet, they will be adjusted later.<br>
There is no need to use a screw for every hole of the rail. Using every 2nd or 3rd will suffice.<br>
Now do the same for the end stops, facing the same direction as in the picture above. Slightly tighten these to prevent the carriage from sliding off the rail.<br>


### Step 6 - Connect bottom and top frame together
<a href="url"><img src="https://github.com/OleIdole/Kossel-XL-DIY-3D-printer/blob/master/Pictures/Frame%20bottom.jpg" align="center" height="302" width="403" ></a> <br>
<a href="url"><img src="https://github.com/OleIdole/Kossel-XL-DIY-3D-printer/blob/master/Pictures/Complete%20frame.jpg" align="center" height="403" width="302" ></a> <br>
First insert the T-nut and screw to the corners, use washers on the outside of the corners.<br>
Then slide the long 20x20 profiles into the bottom frame.<br>
Tighten the bottom frame, then insert 6 T-nuts on the outside of each long 20x20 profile, these are used for the plexi cover later.<br>
Now connert the top frame similar to the bottom frame. Make sure the top frame is flush with the end of the profiles as in the picture below.<br>
<a href="url"><img src="https://github.com/OleIdole/Kossel-XL-DIY-3D-printer/blob/master/Pictures/Frame%20top.jpg" align="center" height="403" width="302" ></a> <br>


### Step 7 - Adjust the linear rails
<a href="url"><img src="https://github.com/OleIdole/Kossel-XL-DIY-3D-printer/blob/master/Pictures/Rails%20top.jpg" align="center" height="403" width="302" ></a> <br>
<a href="url"><img src="https://github.com/OleIdole/Kossel-XL-DIY-3D-printer/blob/master/Pictures/Rail%20bottom.jpg" align="center" height="403" width="302" ></a> <br>
Now that the frame top is in place, adjust the end stops and linear rails according to the pictures above.<br>
Press them up against the top frame and tighten.<br>


### Step 8 - Attach end stops
<a href="url"><img src="https://github.com/OleIdole/Kossel-XL-DIY-3D-printer/blob/master/Pictures/Attach%20end%20stops.jpg" align="center" height="403" width="302" ></a> <br>
Attach the end stops on the top bracket just above the linear rails similar to the picture above.<br>
The Switch must face down, it will detect when the carriage reach the end.<br>


### Step 9 - Attach hotbed mount
<a href="url"><img src="https://github.com/OleIdole/Kossel-XL-DIY-3D-printer/blob/master/Pictures/Hotbed%20mount%20attach.jpg" align="center" height="302" width="403" ></a> <br>
Insert 2 T-nuts on top of each 20x20 profile and attach to the hotbed mount with the 12mm M4 screws.<br>
Do not tighten these yet, they will be positioned when the hotbed is inserted later.<br>


### Step 10 - Attach belt to carriage
<a href="url"><img src="https://github.com/OleIdole/Kossel-XL-DIY-3D-printer/blob/master/Pictures/Belt%20assembly%201.jpg" align="center" height="403" width="302" ></a> <br>
Detach the loose 3D-printed part of the carriage to be able to fit the belt.<br>
Insert the belt end as in the picture above. Then thread it through with the bearing on top of the printer.<br>
Now thread it down through with the tooth pulley on the bottom of the printer.<br>
<a href="url"><img src="https://github.com/OleIdole/Kossel-XL-DIY-3D-printer/blob/master/Pictures/Belt%20assembly%202.jpg" align="center" height="403" width="302" ></a> <br>
Place the belt inside the loose 3D-printed part positioned in a way that you barely reach the nut on the loose part with the screw.<br>
This way you will have the possibility to tighten even more later on if the belt gets some slack.<br>
Tighten the belt until you can barely pinch the belt together, cut the end when satisfied.<br>


### Step 11 - Apply vibration dampers
<a href="url"><img src="https://github.com/OleIdole/Kossel-XL-DIY-3D-printer/blob/master/Pictures/Vibration%20dampers.jpg" align="center" height="403" width="302" ></a> <br>
Apply 2 vibration dampers to each corner as in the picture. These are essential for reducing the noise.<br>


### Step 12 - Attach power supply
<a href="url"><img src="https://github.com/OleIdole/Kossel-XL-DIY-3D-printer/blob/master/Pictures/Power%20supply%20into%20frame.jpg" align="center" height="403" width="302" ></a> <br>
Attach the power supply similar to the picture above. The back end of the power supply should face the front of the printer.<br>
Use washers between the plastic and screws and tighten them to the T-nuts in the frame.<br>


### Step 13 - Attach relay
<a href="url"><img src="https://github.com/OleIdole/Kossel-XL-DIY-3D-printer/blob/master/Pictures/Relay%20connection%201.jpg" align="center" height="403" width="302" ></a>  <a href="url"><img src="https://github.com/OleIdole/Kossel-XL-DIY-3D-printer/blob/master/Pictures/Relay%20connection%202.jpg" align="center" height="403" width="302" ></a> <br>
Before attaching the relay, connect the wires. It is recommended to use ferrules for all wires.<br>
Connect a black wire of 1.5mm2 with length 40cm to number 1(output).<br>
Connect another black wire of same length and dimension to number 4(- input).<br>
Connect a red wire of same length and dimension to number 3(+ input).<br>
Strip down the insulation of the orange heatbed cable about 23cm from the circle.<br>
Connect the black wire from that cable to number 2(output).
<br>
There is nothing wrong with using different colors for the wires, but it is recommended to keep it organized.<br>
Now attach the relay to the power supply bracket similar to the picture above.<br>


### Step 14 - Attach ramps 1.4 box
<a href="url"><img src="https://github.com/OleIdole/Kossel-XL-DIY-3D-printer/blob/master/Pictures/Ramps%20box%20position.jpg" align="center" height="403" width="302" ></a> <br>
Insert the Ramps 1.4 into the box, then attach the box onto the two nuts on the right side 20x20 profile.<br>


### Step 15 - Attach the fan holder
<a href="url"><img src="https://github.com/OleIdole/Kossel-XL-DIY-3D-printer/blob/master/Pictures/Fan%20holder%20attached.jpg" align="center" height="302" width="403" ></a>  <a href="url"><img src="https://github.com/OleIdole/Kossel-XL-DIY-3D-printer/blob/master/Pictures/Fan%20holder%20fan%20cable%20location.jpg" align="center" height="403" width="302" ></a> <br>
Pull the cables through the frame, the power wires should go straight in, while the fan wires should go through next to the open part of the ramps box.<br>
Attach the fan holder on the outside in front of the ramps box using T-nuts.<br>
Make sure the fans are positions as in the picture to ensure proper cooling on the stepper drivers.<br>


### Step 16 - Attach the filament holder
Attach filament holder on the left side bottom frame as close to the front as possible.<br>
Attach the cylinder to the filament holder with the longest threads towards the filament holder.<br>
To add filament, place the filament spool on the cylinder, then secure it with the nut.<br>
Once finished it should look similar to the picture below.<br>
<a href="url"><img src="nettsidelenke her" align="center" height="302" width="403" ></a>


### Step 17 - Attach the extruder
Attach extruder bracket on the left side bottom frame as close to the back as possible.<br>
Attach the gear onto the motor with the set screw facing motor.<br>
Position the gear such that the filament going through is centered in the gear teeth.<br>
Attach the motor onto the bracket with the plug pointing up and away from the printer.<br>
It should look like in the picture below.<br>
<a href="url"><img src="nettsidelenke her" align="center" height="302" width="403" ></a>

Attach the ...

fest ene siden av den løse 3D-printet delen på motor
sett inn kulelager og fest med skrue
kutt fjær
sett på justerings hjul på skruen
sett på skruen med fjær mellom løs og fast 3D-printet del


### Step 18 - Attach the LCD display
plugg ledning inn i ramps
så plugg ledning inn i LCD
så sett LCD inn i LCD boks
så sett boksen på fremside 20x20 profil bunn ramme


### Step 19 - Attach the hotend
først sette på 3D-printet hotend
så sett på viftene
så sett på stenger
så fest stenger på vognene
så sett på filament slange og ledninger til viftene
så sett på beskyttelses slange rundt ledningene og filament slangen


### Step 20 - Wiring
(Sett inn bilde av koblingsskjema her)
