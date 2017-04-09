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
// Center-to-center distance of the holes in the diagonal push rods. <br>
DELTA_DIAGONAL_ROD

// Horizontal offset from middle of printer to smooth rod center. <br>
DELTA_SMOOTH_ROD_OFFSET

// Horizontal offset of the universal joints on the end effector. <br>
DELTA_EFFECTOR_OFFSET

// Horizontal offset of the universal joints on the carriages. <br>
DELTA_CARRIAGE_OFFSET

// Print surface diameter/2 minus unreachable space (avoid collisions with vertical towers). <br>
DELTA_PRINTABLE_RADIUS

Fill in you measurements in the Configuration.h 

For our printer we have this masurements. 

<a href="url"><img src="https://github.com/OleIdole/Kossel-XL-DIY-3D-printer/blob/master/Pictures/Kossel_Calibration.png" align="center" height="515" width="662" ></a> <br>

Filament rounout sensor: <br> 
http://3dmodularsystems.com/en/upgrades/275-runout-sensor-module-for-reprap-3d-printers.html
