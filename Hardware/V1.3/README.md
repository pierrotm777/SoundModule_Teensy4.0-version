# Hardwares
My PCB use Kicad 9.0.6  

# What news with this version
- Replaced the old regulator with a L1117 5V.  
- Adding a 1N5819 Schottky diode for safety.  
- Separated the power supply for the tank; it will be powered by an external adjustable 6V 3A power supply.  
- Adding the transformer and a capacitor before the MOSFET, necessary for using a piezo humidifier.  
- Replaced the MOSFET with OA3400, which freed up space for the transformer.  
- Adding an I2C connecteur for new features.  
- Use **Serial1** for **CRSF or Telemetry** uses (replace the Serial0 in v1.1 and v1.2).  

## Schematics v1.3
<table border="2">
<tr>
<td><img src="https://github.com/pierrotm777/SoundModule_Teensy4.0-version/blob/main/Hardware/V1.3/Sound_Myca_Teensy_Top.jpg" border="0"/></td>
</tr>
</table>

## PCB v1.3
<table border="2">
<tr>
<td><img src="https://github.com/pierrotm777/SoundModule_Teensy4.0-version/blob/main/Hardware/V1.3/Sound_Myca_Teensy_Top.jpg" border="0"/></td>
<td><img src="https://github.com/pierrotm777/SoundModule_Teensy4.0-version/blob/main/Hardware/V1.3/Sound_Myca_Teensy_Bot.jpg" border="0"/></td>
</tr>
</table>

# Firmwares

1. Two modes are always possibles:  
  - X-Any.  
  - Buttons Keypad.  
1. New features:  
There have been improvements since version v1.2.  
For version 3.9 and up:
  - Telemetries versions usable, S-PORT, HUB, IBUS, CRSF, HOTT, MLINK, RADIOLINK and JETIEX.  
  - Adding a Wi-Fi connection (ESPNOW) via an ESPC3 LCD for.  
  (Allows you to check the proper functioning of the Teensy using the BURC ESP32 screen).  

