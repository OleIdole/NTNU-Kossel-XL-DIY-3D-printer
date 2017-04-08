legg inn bilde ved link: ![alt tag](x) <br>
eller for å kunne skalere: <a href="url"><img src="link" align="center" height="400" width="400" ></a> <br>
ny linje: <br>

## Preparation of parts

### Step 1 - Tie rod carbon tubes
<a href="url"><img src="https://github.com/OleIdole/Kossel-XL-DIY-3D-printer/blob/master/Pictures/Carbon%20rod.jpg" align="center" height="403" width="302" ></a> <br>
Apply glue to the tie rod end and insert it into the tie rod carbon tube. **Avoid applying glue to the bearing.**<br>
Loctite Power Epoxy Universal works well for this, but other types can also work.<br>
**Make sure that the tie rod ends does not slide out while the glue dries.**<br>
**Make sure that the tie rod ends on both sides are equally rotated.**<br>

### Step 2 - Carriage
<a href="url"><img src="https://github.com/OleIdole/Kossel-XL-DIY-3D-printer/blob/master/Pictures/Carriage.jpg" align="center" height="403" width="302" ></a> <br>
**Make sure the carriage does not slide off the linear rail, there are loose parts inside!**<br>
Assemble the carriage similar to the picture. These will later be used to keep the belt tightened and also move the delta arms.<br>


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


### Step 4 - Power supply voltage
<a href="url"><img src="https://github.com/OleIdole/Kossel-XL-DIY-3D-printer/blob/master/Pictures/Power%20supply%20voltage%20switch%201.jpg" align="center" height="403" width="302" ></a>
<a href="url"><img src="https://github.com/OleIdole/Kossel-XL-DIY-3D-printer/blob/master/Pictures/Power%20supply%20voltage%20switch%202.jpg" align="center" height="403" width="302" ></a> <br>
It is important to change the voltage setting of the power supply before it is used.<br>
Since we operate with 230V we have to flip the switch from 115V to 230V on the side of the power supply.<br>

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


## Assembly

### Step 1 - Insert T-nuts into the short 20x20 profiles
<a href="url"><img src="https://github.com/OleIdole/Kossel-XL-DIY-3D-printer/blob/master/Pictures/T-nut.jpg" align="center" height="403" width="302"></a> <br>
**This part is for the profiles on the bottom section, not the top part of the printer**<br>
Insert T-nuts into the 20x20 profiles according to the list below:<br>
<br>
**Front:**<br>
Lower outside: 2<br>
Upper outside: 2<br>
Lower inside : 5<br>
Upper inside : 5<br>
<br>
**Left side:**<br>
Lower outside: 2<br>
Upper outside: 2<br>
Lower inside : 8<br>
Upper inside : 4<br>
<br>
**Right side:**<br>
Lower outside: 1<br>
Upper outside: 2<br>
Lower inside : 6<br>
Upper inside : 6<br>
<br>

#### Dette skal lenger ned i guiden, beholder her midlertidig.
Inside of all towers (the long 20x20 profiles):<br>
lowest 1 x m4, in the midle 7 x m3 and on topp 1 x m4 <br>
Depends on the carry profile that is used. We used one with 24xm3 holes. <br>
And we used m4 for the end brackets. (lower and upper) 
Right outside tower : 6 <br>
left outside tower : 6 <br>
front outside tower : 6 <br>

Mount 6 on each lower cornerpart and 3 on the upper corners. <br>


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


### Step 5 - Attach linear rails and end stops
**Make sure the carriage does not slide off the linear rail, there are loose parts inside!**<br>
<a href="url"><img src="https://github.com/OleIdole/Kossel-XL-DIY-3D-printer/blob/master/Pictures/Linear%20rail.jpg" align="center" height="403" width="302" ></a> <br>
Assemble the linear rail to the long 20x20 profile using the 3D-printed T-nuts.<br>
Do not tighten this yet, they will be adjusted later.<br>
There is no need to use a screw for every hole of the rail. Using every 2nd or 3rd will suffice.<br>
Now do the same for the end stops, facing the same direction as in the picture above. Slightly tighten these to prevent the carriage from sliding off the rail.<br>


### Step 6 - Connect bottom and top frame together
<a href="url"><img src="https://github.com/OleIdole/Kossel-XL-DIY-3D-printer/blob/master/Pictures/Frame%20bottom.jpg" align="center" height="302" width="403" ></a> <br>
<a href="url"><img src="https://github.com/OleIdole/Kossel-XL-DIY-3D-printer/blob/master/Pictures/Complete%20frame.jpg" align="center" height="403" width="302" ></a> <br>
First insert the T-nut and screw to the corners, then slide the long 20x20 profiles into the bottom frame.<br>
Tighten the bottom frame, then do the same for the top frame. Make sure the top frame is flush with the end of the profiles as in the picture below.<br>
<a href="url"><img src="https://github.com/OleIdole/Kossel-XL-DIY-3D-printer/blob/master/Pictures/Frame%20top.jpg" align="center" height="403" width="302" ></a> <br>


### Step 7 - Adjust the linear rails
<a href="url"><img src="https://github.com/OleIdole/Kossel-XL-DIY-3D-printer/blob/master/Pictures/Rails%20top.jpg" align="center" height="403" width="302" ></a> <br>
<a href="url"><img src="https://github.com/OleIdole/Kossel-XL-DIY-3D-printer/blob/master/Pictures/Rail%20bottom.jpg" align="center" height="403" width="302" ></a> <br>
Now that the frame top is in place, adjust the end stops and linear rails according to the pictures above.<br>
Press them up against the top frame and tighten.<br>

### Step 8


### Step 9


### Step 10


### Step 11


### Step 12
