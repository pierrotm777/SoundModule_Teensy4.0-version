# Hardwares
My PCB use Kicad 9.0.  

# What news with this version
This version solve forgotten wire between SD and Teensy.  
Add CRSF option.  
With CRSF it's possible to have a full telemetry if needed.  

## Schematics v1.2
<table border="2">
<tr>
<td><img src="https://github.com/pierrotm777/SoundModule_Teensy4.0-version/blob/main/Hardware/V1.2/Sound_Myca_Teensy_v1.2.png" border="0"/></td>
</tr>
</table>

## PCB v1.2
<table border="2">
<tr>
<td><img src="https://github.com/pierrotm777/SoundModule_Teensy4.0-version/blob/main/Hardware/V1.2/Sound_Myca_Teensy_Top_v1.2.png" border="0"/></td>
<td><img src="https://github.com/pierrotm777/SoundModule_Teensy4.0-version/blob/main/Hardware/V1.2/Sound_Myca_Teensy_Bot_v1.2.png" border="0"/></td>
</tr>
</table>

# Firmwares
Two modes are possibles:
- X-Any.
- Buttons Keypad. 

# Last changes
In this version, the tank is powered by the +5v and it's not enought.  
For  better smoke performance, it's possible to use a +6v DCDC module as power.  
How to do:  
- cut +5v wire on J9.
- cut the wire between **Out and HP 18w connector**.  
- add a wire between Hp 18w and J9.  
- connect a dcdc buck +6v 3A moduyle on HP 18w.  
- use **Out and a GND pins** for new HP conection.  
![](https://github.com/pierrotm777/SoundModule_Teensy4.0-version/blob/main/Hardware/V1.2/Modify%20Tank%20Power.png)  

