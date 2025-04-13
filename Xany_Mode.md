## Xany Serial Commands
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