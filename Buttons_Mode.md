## Buttons Serial Commands
On Start Buttons mode:  
```
oO Settings Oo
SBUS [ Buttons ] use Channel 6
NO Telemetry in use.
SD Card   : Ready
ENG.LIST  : BF109, CAT-C32, DIESEL, DIESEL7, DSL-120, DSL-180, DSL-BIG, DSL-LTL, DSL-OLD, DSL-TUG, DSL-TURB, DSL-V12, MOTOR, PT-BOAT, SCAN-250, SCAN-V12, VAPEUR
Engine   1: Ready (Boat Mode) Name:MOTOR Use Ch:2 (Start by Stick's Motor)
Volume    : Use Ch:5 (Limited Vol:0.10)
Ambient   : (Off) Use Ch:3
Amb. Rnd. : (Off) Use Ch:15
Fog       : (Off) Use Ch:4
Anchor    : (Off) Use Ch:8
Action    : (Off) Use Xany
Action2   : (Off) Use Xany
Smoke     : (On)  Use Ch:14
Engine Spd: 4
ESC       : (On) 
Smoke Ach : 2
Smoke Min : 40
Smoke Max : 126
Sounds 2x8: (Off) Use Ch:16
Mini Ch   : 1000
Maxi Ch   : 2000
Pulses    : (00000000) = 0
```

Help Buttons Help:  
H  
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
S4 X=Ch set Ambients Random Ch
S5 X=Ch set Motor Ch
S6 X=Ch set Action1 Ch
S7 X=Ch set Action2 Ch
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
U6 X=10 to 50 set Minimum Smoke
U7 X=100 to 255 set Maximum Smoke
U8 X=1 to 10 set Engine Speed
U9  X=0 or 1 set ESC On Off
U10 X set Anchor SoundD STOP after X seconds
V X X=Ch Set Volume Ch (Ch=100 if by XANY)
M Check Min and Max Channel
P X Y X=0 to 13 (Sound) / Y=1 to 4 (Start/Idle/Stop, 4=PRINT SOUNDS)
A X X=NAME (Read NAME.wav file from root SDcard).
D Debug Mode On/Off
L Y Y=100 to 255 ms
```