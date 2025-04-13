## Xany Compatibility
All RC systems are not compatible with the Xany protocol.  

### Usable system with Xany

Compte rendu bon fonctionnement Xany:  
Les tests ont tous été réalisés avec un Teensy 4.0 et Xany2Spy sw=8 et sw=16.  

System|Type|Output|Repeat|Filter|
|:---|:---|:---|:---|:---|
|FrskyX|PWM/SBUS|SORTIES +-100%|R=2|F=0|
|FlySky|PWM/IBUS/SBUS/PPM|SORTIES +-100%|R=2|F=2|
|Graupner|PWM/SUMD|SORTIES +-100%|R=1|F=0| 
|Hitec|PWM |SORTIES +-100%|R=1|F=1|
|Spektrum|PWM|SORTIES +-132%|R=1|F=0|

Graupner SUMD non testé mais très probablement fonctionnel.  
Multiplex n'est pas compatible Xany :-(  
