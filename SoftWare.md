
# Setting up software (Cura and Pronterface)

## Cura (slicer software)

Download the newest version of Cura at Ultimaker's official website, [click here.](https://ultimaker.com/en/products/cura-software)<br>

First you must add the printer as it is not part of the default printers in Cura. Go to settings > printer > add printer.<br>
Select custom > custom FDM printer, then you need to enter all the settings for the printer.<br>

Enter the settings as shown in the picture below.
<a href="url"><img src="https://github.com/OleIdole/NTNU-Kossel-XL-DIY-3D-printer/blob/master/Pictures/Cura%20printer%20settings.png" align="center" height="512" width="634" ></a> <br>

Start Gcode:
```
G28
G1 X110 Y45 F3000
G92 E0
G1 Z30
G1 E10 F225
G1 X80 Y60 F3000
G92 E0
```

End Gcode:
```
M104 S0 ;extruder heater off
M140 S0 ;heated bed heater off (if you have it)
G91 ;relative positioning
G1 E-1 F300  ;retract the filament a bit before lifting the nozzle, to release some of the pressure
G28 ;Home all axes (max endstops)
M84 ;steppers off
G90 ;absolute positioning
```
