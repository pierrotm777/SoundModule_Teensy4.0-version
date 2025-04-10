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
- X-Any version, use the hex file **teensy_sound_Xany_V2.1.XANY.hex**.  
- Buttons version, use the hex file **teensy_sound_Xany_V2.1.BUTTONS.hex**.  

For upload a firmware into the Teensy you must to use the [Teensy Loader](https://github.com/pierrotm777/SoundModule_Teensy4.0-version/tree/main/Firmware/Teensy_Uploader.zip).  

## Serial Commands
On Start Xany mode:
```
Sound Module (by croby_b). Apr  9 2025 11:10:57 V2.2 (PCB V1.2 by pierrotm777)
		 oOO Powered by Rc-Navy Libraries OOo 

IBUS [ Xany ] use Channels 6(1) and 7(2) | Filter:0 | SW:16(1) SW:8 + PROP(RCUL5)
NO Telemetry in use.
Engine   1: not Ready (Boat Mode) Name:MOTOR Use Ch:2 (Start by Xany)
SD card OK !
StartSound:/ENGINES/MOTOR_STA.wav
IdleSound: /ENGINES/MOTOR_IDL.wav
StopSound: /ENGINES/MOTOR_STP.wav
SlowSound: /ENGINES/MOTOR_SLW.wav
Alarms Priorities: 0 0 0 0 
Ws2812b Setup done !
End Setup !
```

On Start Buttons mode:
```
Sound Module (by croby_b). Apr 10 2025 08:04:39 V2.2 (PCB V1.2 by pierrotm777)
		 oOO Powered by Rc-Navy Libraries OOo 

SBUS [ Buttons ] use Channel 7
NO Telemetry in use.
Engine   1: not Ready (Boat Mode) Name:MOTOR Use Ch:2 (Start by Xany)
SD card OK !
StartSound:/ENGINES/MOTOR_STA.wav
IdleSound: /ENGINES/MOTOR_IDL.wav
StopSound: /ENGINES/MOTOR_STP.wav
SlowSound: /ENGINES/MOTOR_SLW.wav
Alarms Priorities: 0 0 0 0 

********************
Change Volume Channel!
Change Ambient Channel!
Change Fog Channel!
Change Anchor Channel!
Change Smoke Channel!
Change AutoStart to 'false'!
********************

Ws2812b Setup done !
End Setup !
```

Help Xany Menu:
H
```
H Help
SW set Default settings
S? Read Settings
W? Board Connections
SI X X=1(PWM), X=2(CPPM), X=3(SBUS), X=4(IBUS), X=5(SUMD), X=6(JETI), X=7(SRXL), X=8(CRSF)
SX Y Z Y=0 to 16 Xany 0=OFF 1 to 16=Xany Channel / Z=1 to 4 Xany mode
SY Y Z Y=0 to 16 Xany 0=OFF 1 to 16=Xany Channel / Z=1 to 4 Xany mode
F X X=0 to 3 Set Xany filter
R set Ambient On/Off
S1 X=Ch set Ambient Ch
S2 X=Ch set Fog Ch
S3 X=Ch set Anchor Ch
S4 X=Ch set Ambients Random Ch
G Y=0 or 1 set Xany=0 Buttons=1
X1 Y Y=0 to 2 Debug RCUL1 Mode
X5 Y Y=0 to 2 Debug RCUL5 Mode
U0 set Smoke On/Off
U1 X=Ch set Engine Ch
U2 X=0 or 1 set Engine Mode
U3 X=name set Engine Name
U4 X set Engine/Smoke STOP after X seconds
U5 X=Ch set Smoke On/Off Ch
I I=XXXX X=N or P (Alarms Priorities
V X X=Ch Set Volume Ch (Ch=0 if by XANY
M Check Min and Max Channel
P X Y X=0 to 13 (Sound) / Y=1 to 4 (Start/Idle/Stop, 4=PRINT SOUNDS)
A X X=NAME (Read NAME.wav file from root SDcard).
D Debug Mode On/Off
X1 Y Y=0 to 2 Debug RCUL1 Mode
X5 Y Y=0 to 2 Debug RCUL5 Mode
```

Help Buttons Help:
```
H Help
SW set Default settings
S? Read Settings
W? Board Connections
SI X X=1(PWM), X=2(CPPM), X=3(SBUS), X=4(IBUS), X=5(SUMD), X=6(JETI), X=7(SRXL), X=8(CRSF)
R set Ambient On/Off
S1 X=Ch set Ambient Ch
S2 X=Ch set Fog Ch
S3 X=Ch set Anchor Ch
T Start/Stop Buttons Calibration
C Start Buttons Values
B Read Buttons Values
O O=XXXXXXXX X=0 or 1 (Pulse Modes
U0 set Smoke On/Off
U1 X=Ch set Engine Ch
U2 X=0 or 1 set Engine Mode
U3 X=name set Engine Name
U4 X set Engine/Smoke STOP after X seconds
U5 X=Ch set Smoke On/Off Ch
I I=XXXX X=N or P (Alarms Priorities
V X X=Ch Set Volume Ch (Ch=0 if by XANY
M Check Min and Max Channel
P X Y X=0 to 13 (Sound) / Y=1 to 4 (Start/Idle/Stop, 4=PRINT SOUNDS)
A X X=NAME (Read NAME.wav file from root SDcard).
D Debug Mode On/Off
```

S?
```
oO Settings Oo
IBUS [ Xany ] use Channels 6(1) and 7(2) | Filter:0 | SW:16(1) SW:8 + PROP(RCUL5)
NO Telemetry in use.
SD Card   : Ready
ENG.LIST  : BF109, CAT-C32, DIESEL, DIESEL7, DSL-120, DSL-180, DSL-BIG, DSL-LTL, DSL-OLD, DSL-TUG, DSL-TURB, DSL-V12, MOTOR, PT-BOAT, SCAN-250, SCAN-V12, VAPEUR
Engine   1: Ready (Boat Mode) Name:MOTOR Use Ch:2 (Start by Xany)
Volume    : Use Xany (Limited Vol:0.10)
Ambient   : (Off) Use Xany
Amb. Rnd. : (Off) Use Ch:15
Fog       : (Off) Use Xany
Anchor    : (Off) Use Xany
Smoke     : (Off) Use Xany
Priorities: 0000 (Alarms Sounds)
Mini Ch   : 1000
Maxi Ch   : 2000
```