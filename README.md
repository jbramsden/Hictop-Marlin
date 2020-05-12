# Hictop-Marlin
Marlin configuration files for a Hictop 3D printer

## Introduction
These are my configuration files for Marlin 2.0.x for my Hictop 3D printer. 
The changes are based of vlachoudis hard work on https://www.thingiverse.com/thing:2829405 for Marlin version 1.1.9

## Changes to my printer from the Standard Hictop
I have made only two changes so far to my standard Hictop Prusa clone.
The first being a SN04 probe. 
The second being a E3D Chimera dual extruder. 

## Comments in the file for the Hictop changes and my custom changes
All Hictop changes have a comment of //Hictop within the file.
For the E3D changes there is also //Hictop E3d Chimera. 
Please note that when you see a ( ) after the Hictop comment with a number in between this will be the default setting for Hictop, but I have customised this for my printer.

## Reference URLs
⋅ Marlin firmware: https://github.com/MarlinFirmware/Marlin
⋅ Hictop firmware: https://www.hic3dprinter.com/pages/firmware
⋅ E3D Chimera documents on firmware changes: https://e3d-online.dozuki.com/Guide/Chimera+Marlin+Configuration/31?lang=en

## Changes made to configuration.h
For a quick refernece of all the changes made in the file:
```c
#define BAUDRATE 115200 //Hictop
#define MOTHERBOARD BOARD_RAMPS_13_EFB //Hictop
#define CUSTOM_MACHINE_NAME "Hictop E3D" //Hictop
#define EXTRUDERS 2 //Hictop E3D Chimera
#define DEFAULT_NOMINAL_FILAMENT_DIA 1.75 //Hictop E3D Chimera
#define TEMP_SENSOR_0 5    // Hictop(3) E3D Chimera
#define TEMP_SENSOR_1 5    // Hictop(0) E3D Chimera
#define TEMP_SENSOR_BED 3   // Hictop
#define HEATER_0_MAXTEMP 285  //Hictop(275) E3D Chimera
#define HEATER_1_MAXTEMP 285  //Hictop(275) E3D Chimera
#define X_MIN_ENDSTOP_INVERTING true // Hictop Set to true to invert the logic of the endstop.
#define Y_MIN_ENDSTOP_INVERTING true // Hictop Set to true to invert the logic of the endstop.
#define Z_MIN_ENDSTOP_INVERTING true // Hictop Set to true to invert the logic of the endstop.
#define X_MAX_ENDSTOP_INVERTING true // Hictop Set to true to invert the logic of the endstop.
#define Y_MAX_ENDSTOP_INVERTING true // Hictop Set to true to invert the logic of the endstop.
#define Z_MAX_ENDSTOP_INVERTING true // Hictop Set to true to invert the logic of the endstop.
#define Z_MIN_PROBE_ENDSTOP_INVERTING true // Hictop Set to true to invert the logic of the probe.
#define DEFAULT_AXIS_STEPS_PER_UNIT   { 80, 80, 398, 94.4962144 } // Hictop
#define FIX_MOUNTED_PROBE // Hictop
#define NOZZLE_TO_PROBE_OFFSET { -10, -10, -0.5 } // Hictop
#define INVERT_Y_DIR false  // Hictop
#define INVERT_Z_DIR true // Hictop
#define X_BED_SIZE 210   // Hictop
#define Y_BED_SIZE 270   // Hictop
#define FIL_RUNOUT_INVERTING true // Hictop Set to true to invert the logic of the sensor.
#define FIL_RUNOUT_PIN     11       // Hictop+BNV, instead of pins_RAMPS.h
//#define AUTO_BED_LEVELING_LINEAR  //Hictop
#define AUTO_BED_LEVELING_BILINEAR
#define LEFT_PROBE_BED_POSITION 3    // Hictop
#define RIGHT_PROBE_BED_POSITION 175          // Hictop
#define FRONT_PROBE_BED_POSITION 3            // Hictop
#define BACK_PROBE_BED_POSITION 180           // Hictop
#define LCD_BED_LEVELING  // Hictop SN04 bed level probe
#define PREHEAT_1_TEMP_HOTEND 200 //Hictop(180) E3D
#define PREHEAT_1_TEMP_BED     60 //Hictop(70) E3D
#define SDSUPPORT //Hictop
#define SPI_SPEED SPI_SIXTEENTH_SPEED    // Hictop
#define REPRAP_DISCOUNT_SMART_CONTROLLER  // Hictop
```
## Changes made to configuration_adv.h
For a quick refernece of all the changes made in the file:
```c
#define ADVANCED_PAUSE_FEATURE // Hictop
```


