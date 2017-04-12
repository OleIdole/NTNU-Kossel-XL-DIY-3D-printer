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
  #endif
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
