## Links to parts for 3D printing 

Frame:      http://www.thingiverse.com/thing:2050125 <br>
Effector:   http://www.thingiverse.com/thing:1569106 <br>
Extruder:   http://www.thingiverse.com/thing:662885 <br>
      or    http://www.thingiverse.com/thing:1327931 <br>
Carriage:   http://www.thingiverse.com/thing:1253123 <br>
            http://www.thingiverse.com/thing:858871   (Used the endstops) <br>
Heatbedholder: 2 4mx25mm screw, 5mmx20mm spring .


## Remember Ramps 1.4 
There are 3 jumper settings under the stepper
Jumpers need to be installed under each stepper driver:

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
 
 If the jumpers set it to a higher number of micro steps than supported by the 
 driver it will operate at the maximum number of micro steps for that driver. 
 Sinse we use the pololu A4988 stepper motor drivere, that results in 1/16 micro stepping



Guide for mounting the E3D V6 

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

Mount 6 on each lower cornerpart and 3 on the upper corners. 



