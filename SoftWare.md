
# Setting up software (Cura and Pronterface)

## Cura (slicer software)

Download the newest version of Cura at Ultimaker's official website, [click here.](https://ultimaker.com/en/products/cura-software)<br>

### Printer settings
First you must add the printer as it is not part of the default printers in Cura.<br>
Go to settings > printer > add printer.<br>
Select custom > custom FDM printer > Give it at decent name like NTNU Kossel > click add printer down to the right.<br>


Enter the settings as shown in the picture below.
<a href="url"><img src="https://github.com/OleIdole/NTNU-Kossel-XL-DIY-3D-printer/blob/master/Pictures/NTNUKosselSetup.PNG" align="center" height="512" width="634" ></a> <br>

You need to select "Marlin" as the GCode flavor and filament diameter to 1.75mm.<br>

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


### Printer profile
The default printer profiles are already quite good, but can be tweaked for better results.<br>
These settings are available on the right half side of Cura, the optimal settings are affected by filament supplier and the printer.<br>
Here are the most important settings that we personally preffer to tweak:<br>
**Note: this is the settings used for PLA**
```
Infill:
Infill Density - this is often edited depending on what you are making. Default should be set around 20%.

Material:
Printing Temperature - different for each filament, test them to find optimal temperature. Around 210*C is common to use.
Build Plate Temperature - around 60*C is normal. You might want to raise it to 70*C if print is not sticking to the build plate.
Diameter - important to keep this at the same as your filament, 1.75mm is standard for this printer.
Flow - this must be tweaked in order to find optimal values. Start out at 100% and try different values. We ended up at 90% flow.
Enable Retraction - this should be enabled to eliminate stringing.

Speed:
Print Speed - this can be tweaked for optimal results, we recommend around 60mm/s.
Travel Speed - this can be tweaked for optimal results, we recommend around 120mm/s.

Cooling:
Enable Print Cooling - this should be enabled for optimal results.

Support:
Enable support - Toggle this for own needs.

Build Plate Adhesion:
Build Plate Adhesion Type - Brim
Brim Width - tweak this for own prefferences. Larger brim means stronger adhesion to build plate.
```

We recommand this profile settings:
<a href="url"><img src="https://github.com/OleIdole/NTNU-Kossel-XL-DIY-3D-printer/blob/master/Pictures/RecomandedPMachinesettings.PNG" height="741" width="405" ></a> <br>


## Pronterface (Manual printer controller)

Download the newest version of Pronterface at their official website, [click here.](http://www.pronterface.com/)<br>

### Connecting to printer
Open Pronterface, then change Port and Baud rate up in the left corner, set Baud rate to 250 000.<br>
