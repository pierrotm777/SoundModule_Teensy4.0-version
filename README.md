# Multi Sounds for RC boat (or Truck, Tank, Car and Plane)

## Credits
Based on a croby-b's code idea.  

## Outline of the documentation
1. Introduction (this page)
1. [Xany Compatibility](Xany_Compatibility.md)
1. [Xany Serial Commands](Xany_Mode.md)
1. [Buttons Serial Commands](Buttons_Mode.md)
1. [Smoke System](Smoke_System.md)  
1. [Wiring Sound module](Wiring_Module.md)


## Introduction
For build this module we use the [Teensy-Variable-Playback](https://github.com/newdigate/teensy-variable-playback) library with a Teensy 4.0.  

Sound Module for Rc boat and Plane.  
- Engine(s) variable sound.  
- Multi Sounds (4 sounds in same time + motor).  
- Smoke (pump and tank) engine command.  
All these sounds are played in same time.  
- Telemetry (CRSF,IBUS,S-PORT).  



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
- CRSF  


### Buttons mode
This mode use a keyboard with 10 buttons (8 buttons + 2 for volume sounds).  
It's a good solution for rc transmitters that do not have a training input.  
This keyboard is connected on a free input channel in place of a potentiometer.  
This mode accept only 8 sounds.  
The buttons 9 and 10 up or down the volume's sounds.  

<table cellspacing=0>
  <tr>
    <td align=center width=400><a href="https://github.com/pierrotm777/SoundModule_Teensy4.0-version/blob/main/10ButtonsKeyboard.md"><img src="https://github.com/pierrotm777/SoundModule_Teensy4.0-version/blob/main/10buttons_sch.png" border="0" name="submit" title="Sound Module" alt="Sound Module"/></a><br><b>KeyBoard 10 buttons</td>
  </tr>
</table>

Depending on the receiver used, it's possible to connect the sound module in different ways:  
- PWM  
- CPPM  
- SBUS (without inverter)  
- IBUS  
- SUMD  
- SRXL  
- JETIEX  
- CRSF  


A **BURC encoder** or a **LVGL ESP32 S3 Screen** is connected on a Handset by CPPM or SBUS.     

**This X-Any/BURC coder use the trainer port as slave and uses up to 3 channels (for the Sound Module) as X-Any fonctions.** 
**X-Any inject three additionals RC channels to a CPPM or SBUS frame for transport messages over these additionals channels.**  
**At reception side, these messages are extracted from these channels corresponding to the additionals channels.**  
**This serial port can be used to transport a message containing the status of a set of switches or set of sound in the Soud Modul case.**  

## PCB versions
<table cellspacing=0>
  <tr>
    <td align=center width=400><a href="https://github.com/pierrotm777/SoundModule_Teensy4.0-version/tree/main/Hardware/V1.0/README.md"><img src="https://github.com/pierrotm777/SoundModule_Teensy4.0-version/blob/main/Hardware/V1.0/Sound_Myca_Teensy-Top3d_v1.0.png" border="0" name="submit" title="Sound Module" alt="Sound Module v1.0"/></a><br><b>V1.0</td>
    <td align=center width=400><a href="https://github.com/pierrotm777/SoundModule_Teensy4.0-version/tree/main/Hardware/V1.1/README.md"><img src="https://github.com/pierrotm777/SoundModule_Teensy4.0-version/blob/main/Hardware/V1.1/Sound_Myca_Teensy_Top_v1.1.png" border="0" name="submit" title="Sound Module" alt="Sound Module v1.1"/></a><br><b>V1.1</td>
    <td align=center width=400><a href="https://github.com/pierrotm777/SoundModule_Teensy4.0-version/tree/main/Hardware/V1.2/README.md"><img src="https://github.com/pierrotm777/SoundModule_Teensy4.0-version/blob/main/Hardware/V1.2/Sound_Myca_Teensy_Top_v1.2.png" border="0" name="submit" title="Sound Module" alt="Sound Module v1.2"/></a><br><b>V1.2</td>
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
You can change the **USER1.wav to USER15.wav by your own sounds**.  
USER16.wav is used as alarms sound.  

## Upload a firmware
- Frsky
  - X-Any version, use the hex file **teensy_sound_Xany_V2.2.XANY_Frsky_S-SPORT.hex**.  
  - Buttons version, use the hex file **teensy_sound_Xany_V2.2.BUTTONS_Frsky_S-SPORT.hex**.  
- FlySky
  - to do
  - to do
- ExpressLRS
  - X-Any version, use the hex file **teensy_sound_Xany_V2.2.XANY_ExpressLRS_CRSF.hex**.  
  - Buttons version, use the hex file **teensy_sound_Xany_V2.2.BUTTONS_ExpressLRS_CRSF.hex**.  

For upload a firmware into the Teensy you must to use the [Teensy Loader](https://github.com/pierrotm777/SoundModule_Teensy4.0-version/tree/main/Firmware/Teensy_Uploader.zip).  

