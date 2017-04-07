legg inn bilde ved link: ![alt tag](x) <br>
eller for å kunne skalere: <a href="url"><img src="link" align="center" height="400" width="400" ></a> <br>
ny linje: <br>

## Preparation of parts

### Step 1 - Tie rod carbon tubes
<a href="url"><img src="https://github.com/OleIdole/Kossel-XL-DIY-3D-printer/blob/master/Pictures/Carbon%20rod.jpg" align="center" height="403" width="302" ></a> <br>
Put glue on the tie rod end and insert it into the tie rod carbon tube. Loctite Power Epoxy Universal works well for this, but other types can also work.<br>
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
 We will use the same settings for all steppers (X,Y,Z,E0,E1).<br>



### Step 4 - Power supply voltage
<a href="url"><img src="https://github.com/OleIdole/Kossel-XL-DIY-3D-printer/blob/master/Pictures/Power%20supply%20voltage%20switch%201.jpg" align="center" height="403" width="302" ></a>
<a href="url"><img src="https://github.com/OleIdole/Kossel-XL-DIY-3D-printer/blob/master/Pictures/Power%20supply%20voltage%20switch%202.jpg" align="center" height="403" width="302" ></a> <br>
It is important to change the voltage setting of the power supply before it is used.<br>
Since we operate with 230V we have to flip the switch from 115V to 230V on the side of the power supply.<br>

### Step 5


### Step 6




## Assembly

### Step 1 - Insert T-nuts
<a href="url"><img src="https://github.com/OleIdole/Kossel-XL-DIY-3D-printer/blob/master/Pictures/T-nut.jpg" align="center" height="403" width="302"></a> <br>
Insert T-nuts according to the list below:
F: Front <br>
L: Left from front<br>
R: Right from front <br>
Number of nuts i the 20x20 profiles. <br>
F-lower outside: 2<br>
F-upper outside: 2<br>
F-lower inside : 1<br>
F-upper inside : 1<br>
L-lower outside: 2<br>
L-upper outside: 2<br>
L-lower inside : 4<br>
L-upper inside : 0<br>
R-lower outside: 1<br>
R-upper outside: 2 <br>
R-lower inside : 2<br>
R-upper inside : 2 <br>
Inside of all towers :lowest 1 x m4, in the midle 7 x m3 and on topp 1 x m4 <br>
Depends on the carry profile that is used. We used one with 24xm3 holes. <br>
And we used m4 for the end brackets. (lower and upper) 
Right outside tower : 6 <br>
left outside tower : 6 <br>
front outside tower : 6 <br>

Mount 6 on each lower cornerpart and 3 on the upper corners. <br>

### Step 2 - Assemble bottom corners
<a href="url"><img src="https://github.com/OleIdole/Kossel-XL-DIY-3D-printer/blob/master/Pictures/Frame%20bottom.jpg" align="center" height="302" width="403" ></a> <br>

### Step 3 - Attach stepper motors
<a href="url"><img src="https://github.com/OleIdole/Kossel-XL-DIY-3D-printer/blob/master/Pictures/Stepper%20motor.jpg" align="center" height="403" width="302" ></a> <br>

### Step 4 - Assemble top corners


### Step 5 - Connect bottom and top together


### Step 6 - Attach linear rails and end stops
**Make sure the carriage does not slide off the linear rail, there are loose parts inside!**<br>

### Step 7


### Step 8


### Step 9


### Step 10


### Step 11


### Step 12
