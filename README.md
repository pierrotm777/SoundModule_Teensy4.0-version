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
- The module read all WAV sounds from a SD card (from /ENGINES folder).  

### X-Any mode
This mode decode the X-Any/BURC stream.  
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
This keyboard is connected on a free input channel in place of a potentiometer.  
This mode accept only 8 sounds.  
The buttons 9 and 10 up or down the volume's sounds.  
![10 buttons board](https://github.com/pierrotm777/SoundModule_Teensy4.0-version/blob/main/10buttons_sch.png)
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

## WAV Sounds
Play **16-bit PCM 44100Hz Stereo** WAV audio samples at variable playback rates on Teensy.  
- Note : this library only works with signed 16-bit integer samples. Floating point samples will not play.  
- For best performance, use SDXC UHS 30MB/sec Application Performance Class 2 (A2) class micro SD-card.  

### Sounds Motor
It's possible to select several motors.  
The module can list all sound's motor found into the SD card [ENGINES folder](https://github.com/pierrotm777/SoundModule_Teensy4.0-version/tree/main/SD_Wav_Files/ENGINES).  
**ENG.LIST = DSL-LTL, DSL-V12, VAPEUR, DSL-OLD, DSL-120, DSL-TURB, DSL-TUG, SCAN-V12, DSL-BIG, DSL-180, DIESEL7, SCAN-250, CAT-C32, BF109**  
Each motor use:  
- A start file,ex:DSL-LTL_STA.  
- An idle file,ex:DSL-LTL_IDL.  
- A stop file,ex:DSL-LTL_STP.  

It's possible to add new motor's sounds.  
The better way, for me, is to use [Audacity](https://www.audacityteam.org) for cut all sound find and save it as 16bits PCM 44100Hz wav file.  

### All other sounds
All other other sounds will have to be copied under the main path.  
See our sounds [here](https://github.com/pierrotm777/SoundModule_Teensy4.0-version/tree/main/SD_Wav_Files).  
