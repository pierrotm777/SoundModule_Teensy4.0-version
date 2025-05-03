# Xany Serial Commands

## On Start Xany mode
```
Sound Module (by croby_b). May  2 2025 19:49:49 V2.5 (PCB V1.2 by pierrotm777)
		 oOO Powered by Rc-Navy Libraries OOo 

SBUS [ Xany by Handset ] use Channels 6(1) and 7(2) | Filter:0 | SW:16(1) SW:8 + PROP(RCUL5)
S-PORT Telemetry in use.
Engine   1: not Ready (Boat Mode) Name:MOTOR Use Ch:2 (Start by Stick's Motor)
SD card OK !
Fichier /CONFIG/USER.txt existant trouvé, mise à jour.
Aucun changement détecté dans les sons utilisateur.
USER1 = /USERSOUND/1_CLAXON.WAV
USER2 = /USERSOUND/2_BRUME.WAV
USER3 = /USERSOUND/3_MOUETTE.WAV
USER4 = /USERSOUND/4_DAUPHIN.WAV
USER5 = /USERSOUND/5_FRUITPASSION.WAV
USER6 = /USERSOUND/6_NIGHTFEVER.WAV
USER7 = /USERSOUND/7_FROMMETOYOU.WAV
USER8 = /USERSOUND/8_FOREVERALWAYS.WAV
USER9 = /USERSOUND/9_ALLTIMEWORLD.WAV
USER10 = /USERSOUND/10_HALAMER.WAV
USER11 = /USERSOUND/11_SEXEDUP.WAV
USER12 = /USERSOUND/12_SUGAR.WAV
USER13 = /USERSOUND/13_SHADEOFPALE.WAV
USER14 = /USERSOUND/14_LIFEOFMARS.WAV
USER15 = /USERSOUND/15_MURATLANTIQUE.WAV
USER16 = /USERSOUND/16_FOLIEGRANDEUR.WAV
StartSound:/ENGINES/MOTOR_STA.wav
IdleSound: /ENGINES/MOTOR_IDL.wav
StopSound: /ENGINES/MOTOR_STP.wav
SlowSound: /ENGINES/MOTOR_SLW.wav
Alarms Priorities: 0 0 0 0 
Ws2812b Setup done !
Type G 0 for Xany mode or G 1 for Handset mode !

End Setup !
```
In this version USERx are replaced by 16 files under /USERSOUN/ folder.  

## Help Xany Menu
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
S5 X=Ch set Motor Ch
S6 X=Ch set Action1 Ch
S7 X=Ch set Action2 Ch
G Y=0 or 1 set Xany=0 Buttons=1
X1 Y Y=0 to 2 Debug RCUL1 Mode
X5 Y Y=0 to 2 Debug RCUL5 Mode
U0 set Smoke On/Off
U1 X=Ch set Engine Ch
U2 X=0 or 1 set Engine Mode
U3 X=name set Engine Name
U4 X set Engine/Smoke STOP after X seconds
U5 X=Ch set Smoke On/Off Ch
U6 X=10 to 50 set Minimum Smoke
U7 X=100 to 255 set Maximum Smoke
U8 X=1 to 10 set Engine Speed
U9  X=0 or 1 set ESC On Off
U10 X set Anchor SoundD STOP after X seconds
I I=XXXX X=N or P (Alarms Priorities)
V X X=Ch Set Volume Ch (Ch=100 if by XANY)
M Check Min and Max Channel
P X Y X=0 to 13 (Sound) / Y=1 to 4 (Start/Idle/Stop, 4=PRINT SOUNDS)
A X X=NAME (Read NAME.wav file from root SDcard).
D Debug Mode On/Off
L Y Y=100 to 255 ms (Check All leds at Y speed)
SV X X=1.0 External Voltage Scale
```

S?  for Screen mode (type G 0)  
```
oO Settings Oo
SBUS [ Xany by Screen ] use Channels 6(1) and 7(2) | Filter:0 | SW:16(1) SW:8 + PROP(RCUL5)
S-PORT Telemetry in use.
SD Card   : Ready
ENG.LIST  : BF109, CAT-C32, DIESEL, DIESEL7, DSL-120, DSL-180, DSL-BIG, DSL-LTL, DSL-OLD, DSL-TUG, DSL-TURB, DSL-V12, MOTOR, PT-BOAT, SCAN-250, SCAN-V12, VAPEUR
Engine   1: Ready (Boat Mode) Name:MOTOR Use Ch:2 (Start by Xany)
Volume    : Use Xany (Limited Vol:0.10)
Ambient   : (Off) Use Xany
Amb. Rnd. : (Off) Use Xany
Fog       : (Off) Use Xany
Anchor    : (Off) Use Xany
Action    : (Off) Use Xany
Action2   : (Off) Use Xany
Smoke     : (Enabled)  (Off) Use Xany
Engine Spd: 4
ESC       : (Enabled)  (Off) Use Xany
Smoke Ach : 2
Smoke Min : 40
Smoke Max : 126
Priorities: 0000 (Alarms Sounds)
Mini Ch   : 1000
Maxi Ch   : 2000
Scale ExtV: 1.26
```

S?  for Handset mode (type G 1)
```
Sound Module V2.5 Powered By Rc-Navy libraries

oO Settings Oo
SBUS [ Xany by Handset ] use Channels 6(1) and 7(2) | Filter:0 | SW:16(1) SW:8 + PROP(RCUL5)
S-PORT Telemetry in use.
SD Card   : Ready
ENG.LIST  : BF109, CAT-C32, DIESEL, DIESEL7, DSL-120, DSL-180, DSL-BIG, DSL-LTL, DSL-OLD, DSL-TUG, DSL-TURB, DSL-V12, MOTOR, PT-BOAT, SCAN-250, SCAN-V12, VAPEUR
Engine   1: not Ready (Boat Mode) Name:MOTOR Use Ch:2 (Start by Stick's Motor)
Volume    : Use Ch:5 (Limited Vol:0.10)
Ambient   : (Off) Use Ch:3
Amb. Rnd. : (Off) Use Ch:15
Fog       : (Off) Use Ch:4
Anchor    : (Off) Use Ch:8
Action    : (Off) Use Ch:12
Action2   : (Off) Use Ch:13
Smoke     : (Enabled)  (Off) Use Ch:14
Engine Spd: 4
ESC       : (Enabled)  (Off) Use Ch:13
Smoke Ach : 2
Smoke Min : 40
Smoke Max : 126
Priorities: 0000 (Alarms Sounds)
Mini Ch   : 1000
Maxi Ch   : 2000
Scale ExtV: 1.26
```

## Explanation of all XANY commands
The following commands appear in XANY mode (G 0)  
	- [Wiring Sound module](Serial_commands_FR.md)  
	- [Wiring Sound module](Serial_commands_EN.md)  