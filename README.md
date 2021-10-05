# Klipper Config for FLSun-SR with Robin Nano v3


This is my Klipper configuration for the FLSun SR with Robin Nano V3 Board.

********************************************************************************************************************************
********************************************************************************************************************************
IMPORTANT: Currently I have several modifications on my printer that may lead to crashes or strange behaviour for your printer.

            * Added magnetic PEI print bed (reduce overall print high about -3mm)
            * Replaced the original heatblock with a original full copper volcano block that is longer then the original.
            * Replaced the original Bowden Extruder with the Sherpa mini
********************************************************************************************************************************            
********************************************************************************************************************************           
            
           
Issues or usefull links I found during the setup process for Klipper:

  * Use Kiauh to install Klipper and all required dependencies 
    https://github.com/th33xitus/kiauh
    
   * Use KIAUH via Putty to get your MCU ID Open KIAUH Interface select 4 Advanced -> 6Get MCU ID and replace the value in line 4 (printer.cfg) with your MCU ID otherwise Klipper can not connect with the Robin Nano V3
    
  * To install the Firmware via SDcard you need to rename the firmware to "Robin_nano_v3.bin" otherwise it will not work
    Reference: https://github.com/KevinOConnor/klipper/blob/master/config/generic-mks-robin-nano-v3.cfg
 
  * For inital Calibration use the following Steps: 
  * Probe Calibration (https://www.klipper3d.org/Probe_Calibrate.html)
  * Delta Calibration (https://www.klipper3d.org/Delta_Calibrate.html#basic-delta-calibration)
  * BED_MESH_CALIBRATE (https://www.klipper3d.org/Bed_Mesh.html)
          
    The Z Offset need to be set in the Macro PREPARE_PRINT. The Z_Offset for the probe can not be used with delta printers because Z is not only 1 axis its the combination of all 3 axis for delta printer and need to be set in a different way with macro z-offset
          
          
   * Use Firmware Retraction
     https://3dp.tumbleweedlabs.com/firmware/klipper-firmware/klipper-calibration-guide/retraction-calibration-with-klippers-tuning-tower-command
     https://www.thingiverse.com/thing:4532977/comments
  
   * Automatic Temp Tower
     https://www.thingiverse.com/thing:4821884
            
