We are using the Marlin firmware. <br>
http://marlinfw.org/docs/basics/introduction.html<br>
Download form: <br>
https://github.com/MarlinFirmware/Marlin
// For a Delta printer replace the configuration files with the files in the
// example_configurations/delta directory.
https://github.com/MarlinFirmware/Marlin/tree/RC/Marlin/example_configurations

PID autotune: <br> 
https://www.3dhubs.com/talk/thread/pid-autotune

Downloade Pronterface form: <br>
http://kliment.kapsi.fi/printrun/


## StartUp<br> 

1. Check endstopps. Type M119 in proterface <br> 
M119 <br>
SENDING:M119 <br>
Reporting endstop status <br>
x_max: open <br>
y_max: open <br>
z_min: TRIGGERED <br>
z_max: open <br>
z_probe: open <br>

Trigger the endstops one by one and run M119 to confirm that they are working. <br> 

2. Measure the offsets. 
// Center-to-center distance of the holes in the diagonal push rods.
DELTA_DIAGONAL_ROD 315.3 // mm

// Horizontal offset from middle of printer to smooth rod center.
DELTA_SMOOTH_ROD_OFFSET 231.0 // mm

// Horizontal offset of the universal joints on the end effector.
#define DELTA_EFFECTOR_OFFSET 25.0 // mm

// Horizontal offset of the universal joints on the carriages.
#define DELTA_CARRIAGE_OFFSET 30.0 // mm


<a href="url"><img src="https://github.com/OleIdole/Kossel-XL-DIY-3D-printer/blob/master/Pictures/Kossel_Calibration.png" align="center" height="515" width="662" ></a> <br>
