# Multi Sounds for RC boat (or RC plane)

## Credits
Based on a croby-b's code idea.  

## Sound Module features
For build this module we use the [Teensy-Variable-Playback](https://github.com/newdigate/teensy-variable-playback) library with a Teensy 4.0.  

Sound Module for Rc boat and Plane.  
- Engine(s) variable sound.  
- Multi Sounds (3 sound in same time).  
- Smoke (pump and tank) engine command.  
All these sounds are played in same time.  

## How it's work
Two modes are possibles:
- Use [X-Any/BURC encoder](https://p-loussouarn-free-fr.translate.goog/arduino/exemple/RCUL/RCUL.html?_x_tr_sch=http&_x_tr_sl=auto&_x_tr_tl=en&_x_tr_hl=en) fonctions by RC-Navy, thanks to him. 
- Use [Buttons Keypad](http://p.loussouarn.free.fr/projet/MS8-V2/MS8-V2.html#Keyboard) fonctions by RC-Navy, thanks to him.

### X-Any mode
This module decode the X-Any/BURC.  
Depending on the receiver used, it's possible to connect the sound module in different ways:
- PWM  
- CPPM  
- SBUS (without inverter)  
- IBUS  
- SUMD  
- SRXL  
- JETIEX  

### Buttons mode
This mode use a keyboard with 10 buttons (8 buttons + 2 for volume sounds).  
It's a good solution for rc transmitters that do not have a training input.  
This keyboard is connected on a freen input channel in place of a potentiometer.  
This mode accept only 8 sounds.  
The buttons 9 and 10 up or down the volume's sounds.  
Depending on the receiver used, it is possible to connect the sound module in different ways:
- PWM  
- CPPM  
- SBUS (without inverter)  
- IBUS  
- SUMD  
- SRXL  
- JETIEX  

A **BURC encoder** or a **LVGL ESP32 S3 Screen** is connected on a Handset by CPPM or SBUS.     

**This X-Any/BURC coder use the trainer port as slave and uses up to 3 channels (for the Sound Module) as X-Any fonctions.** 
**X-Any inject three additionals RC channels to a CPPM or SBUS frame for transport messages over these additionals channels.**  
**At reception side, these messages are extracted from these channels corresponding to the additionals channels.**  
**This serial port can be used to transport a message containing the status of a set of switches or set of sound in the Soud Modul case.**  

## PCB version v1.0
<table cellspacing=0>
  <tr>
    <td align=center width=400><a href="https://github.com/pierrotm777/SoundModule_Teensy4.0-version/blob/main/Hardware/README.md"><img src="https://github.com/pierrotm777/SoundModule_Teensy4.0-version/blob/main/Sound_Myca_Teensy-Top3d.png" border="0" name="submit" title="Sound Module" alt="Sound Module"/></a><br><b>TOP</td>
  </tr>
</table> 
