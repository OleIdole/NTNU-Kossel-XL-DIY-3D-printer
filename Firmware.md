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
1. Eprom 

2. Check endstopps. Type M119 in proterface <br> 
M119 <br>
SENDING:M119 <br>
Reporting endstop status <br>
x_max: open <br>
y_max: open <br>
z_min: TRIGGERED <br>
z_max: open <br>
z_probe: open <br>

Trigger the endstops one by one and run M119 to confirm that they are working. <br> 

3. Measure the offsets. 
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

## Filament rounout sensor: <br> 
http://3dmodularsystems.com/en/upgrades/275-runout-sensor-module-for-reprap-3d-printers.html


1. Configuration.h
Uncomment 
```
#define FILAMENT_RUNOUT_SENSOR // Uncomment for defining a filament runout sensor such as a mechanical or opto endstop to check the existence of filament
// RAMPS-based boards use SERVO3_PIN. For other boards you may need to define FIL_RUNOUT_PIN.
// It is assumed that when logic high = filament available
//                    when logic  low = filament ran out
#if ENABLED(FILAMENT_RUNOUT_SENSOR)
#define FIL_RUNOUT_INVERTING true // set to true to invert the logic of the sensor.
// #define ENDSTOPPULLUP_FIL_RUNOUT // Uncomment to use internal pullup for filament runout pins if the sensor is defined.
#define FILAMENT_RUNOUT_SCRIPT "M600"
#endif
```

2. Configuration_adv.h 
Make shure that  #define FILAMENT_CHANGE_FEATURE is uncommented. <br> 
Mashure the distanse between your hotend and the extruder and fill inn. 

3. pins_RAMPS.h 
Connect the switch to a free digital innput and ground. 
RAMPS-based boards use SERVO3_PIN (D4). For other boards you may need to define FIL_RUNOUT_PIN.<br>
We used D3 
#define FIL_RUNOUT_PIN      3 // D3

4. Max length for extruding
Change the lengt of Extrud max lengt to the langth of your bowden + 100. 
#define EXTRUDE_MAXLENGTH 950 // mm 

## Change Filament when printer is cold 
1. ultralcd.cpp
add this code lines underneath <br>
void lcd_enqueue_filament_change()<br>
roughly in line 765 <br> 

```
    #if ENABLED(FILAMENT_CHANGE_FEATURE)
    void lcd_enqueue_filament_change_pla() { 
        enqueue_and_echo_commands_P(PSTR("M109 S210"));
        enqueue_and_echo_commands_P(PSTR("M600"));
        lcd_filament_change_show_message(FILAMENT_CHANGE_MESSAGE_INIT);      
    }    
  #endif
    #if ENABLED(FILAMENT_CHANGE_FEATURE)
    void lcd_enqueue_filament_change_abs() { 
        enqueue_and_echo_commands_P(PSTR("M109 S240"));
        enqueue_and_echo_commands_P(PSTR("M600"));
        lcd_filament_change_show_message(FILAMENT_CHANGE_MESSAGE_INIT);      
    }    
  #endif
 ```
2. ultralcd.cpp
Add this code lines in the prepare menu. <br>
It has to be in the: <br>
void lcd_prepare_menu(){<br>
... <br>
} <br>
roughly in line 1270 <br> 
   ```
    // 
    // Change Filament.  
    //
    #if ENABLED(FILAMENT_CHANGE_FEATURE)
        MENU_ITEM(function, MSG_FILAMENTCHANGE_PLA, lcd_enqueue_filament_change_pla);
    #endif
    
    #if ENABLED(FILAMENT_CHANGE_FEATURE)
        MENU_ITEM(function, MSG_FILAMENTCHANGE_ABS, lcd_enqueue_filament_change_abs);
    #endif
   ```
    
3.  language_en.h 
change the massage for fillament change to<br>
```
#ifndef MSG_FILAMENT_CHANGE_INIT_1
    #define MSG_FILAMENT_CHANGE_INIT_1          "Wait for start of"
    #define MSG_FILAMENT_CHANGE_INIT_2          "the filament change"
    #define MSG_FILAMENT_CHANGE_INIT_3          "Heating up"
```

<br>
It is inportant to spesify the length of your bowden pipe before using the change filament command. <br>
This is done in Configuration_avd.h <br>
Search for FILAMENT_CHANGE_FEATURE and fill out all the information you need. <br>
```
// Add support for experimental filament exchange support M600; requires display
#if ENABLED(ULTIPANEL)
  #define FILAMENT_CHANGE_FEATURE             // Enable filament exchange menu and M600 g-code (used for runout sensor too)
  #if ENABLED(FILAMENT_CHANGE_FEATURE)
    #define FILAMENT_CHANGE_X_POS 3             // X position of hotend
    #define FILAMENT_CHANGE_Y_POS 3             // Y position of hotend
    #define FILAMENT_CHANGE_Z_ADD 10            // Z addition of hotend (lift)
    #define FILAMENT_CHANGE_XY_FEEDRATE 100     // X and Y axes feedrate in mm/s (also used for delta printers Z axis)
    #define FILAMENT_CHANGE_Z_FEEDRATE 5        // Z axis feedrate in mm/s (not used for delta printers)
    #define FILAMENT_CHANGE_RETRACT_LENGTH 20    // Initial retract in mm
                                                // It is a short retract used immediately after print interrupt before move to filament exchange position
    #define FILAMENT_CHANGE_RETRACT_FEEDRATE 60 // Initial retract feedrate in mm/s
    #define FILAMENT_CHANGE_UNLOAD_LENGTH 950   // Unload filament length from hotend in mm
                                                // Longer length for bowden printers to unload filament from whole bowden tube,
                                                // shorter lenght for printers without bowden to unload filament from extruder only,
                                                // 0 to disable unloading for manual unloading
    #define FILAMENT_CHANGE_UNLOAD_FEEDRATE 60  // Unload filament feedrate in mm/s - filament unloading can be fast
    #define FILAMENT_CHANGE_LOAD_LENGTH 700     // Load filament length over hotend in mm
                                                // Longer length for bowden printers to fast load filament into whole bowden tube over the hotend,
                                                // Short or zero length for printers without bowden where loading is not used
    #define FILAMENT_CHANGE_LOAD_FEEDRATE 60    // Load filament feedrate in mm/s - filament loading into the bowden tube can be fast
    #define FILAMENT_CHANGE_EXTRUDE_LENGTH 30   // Extrude filament length in mm after filament is load over the hotend,
                                                // 0 to disable for manual extrusion
                                                // Filament can be extruded repeatedly from the filament exchange menu to fill the hotend,
                                                // or until outcoming filament color is not clear for filament color change
    #define FILAMENT_CHANGE_EXTRUDE_FEEDRATE 8  // Extrude filament feedrate in mm/s - must be slower than load feedrate
  #endif
#endif
```


<br> 
M119 - Endstop States
