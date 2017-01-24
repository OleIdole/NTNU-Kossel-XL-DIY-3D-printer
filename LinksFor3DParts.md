## Links to parts for 3D printing 

Frame:      http://www.thingiverse.com/thing:2050125
Effector:   http://www.thingiverse.com/thing:1569106
Extruder:   http://www.thingiverse.com/thing:662885
      or    http://www.thingiverse.com/thing:1327931
Carriage:   http://www.thingiverse.com/thing:1253123
            http://www.thingiverse.com/thing:858871   (Used the endstops) 
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

