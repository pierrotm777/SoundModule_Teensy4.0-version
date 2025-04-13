## Buttons Serial Commands
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