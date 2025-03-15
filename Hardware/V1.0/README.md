# Hardwares
My PCB use Kicad 9.0.  

## Schematics v1.0
<table border="2">
<tr>
<td><img src="https://github.com/pierrotm777/SoundModule_Teensy4.0-version/blob/main/Hardware/V1.0/Sound_Myca_Teensy_v1.0.png" border="0"/></td>
</tr>
</table>

## PCB v1.0
<table border="2">
<tr>
<td><img src="https://github.com/pierrotm777/SoundModule_Teensy4.0-version/blob/main/Hardware/V1.0/Sound_Myca_Teensy-Top3d_v1.0.png" border="0"/></td>
<td><img src="https://github.com/pierrotm777/SoundModule_Teensy4.0-version/blob/main/Hardware/V1.0/Sound_Myca_Teensy-Bot3d_v1.0.png" border="0"/></td>
</tr>
</table>

# Firmwares
Two modes are possibles:
- X-Any.
- Buttons Keypad. 

## Solve unconnected wire
On this version, I have forgotten one wire between SD and Teensy (SCK wire).  
You must connect Pin4(SD) to Pin13(Teensy).  
![add this wire](https://github.com/pierrotm777/SoundModule_Teensy4.0-version/blob/main/Hardware/V1.0/add_wire.png)  

## Add voltage divider bridge
It's possible to read input voltage on pin 15  
![add this wire](https://github.com/pierrotm777/SoundModule_Teensy4.0-version/blob/main/Hardware/V1.0/Add_3S_Input.png)  


