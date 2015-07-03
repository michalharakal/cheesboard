# Arduino IDE #

The huge advanvantage of arduino is the software. The editor with intgrated serial monitor, compiler and uploder for the compiled software makes the debelopment simplier. So we want to have BILDuino integrated into arduino software. It means:
  * definition for board
  * BILDuino core library (patched arduino for ATMEGA32/644)
  * additional libraries for LCD, UI

## Board definition ##
The definitions for boards are in the file _board.txt_. We have to add following block into the file


```
lcdi2c.name=BILDuino
lcdi2c.upload.using=avr910

lcdi2c.build.mcu=atmega32
lcdi2c.build.f_cpu=14745600UL
lcdi2c.build.core=BILDuino
##############################################################
```

## Programmer ##
The existing PCBs have connector for RS232, but only Rx/Tx signals are used, there is no support for DTR(used in arduino for reseting into bootloader) and there is no reset button (never ever build device without reset button !!!) so we will work with external ISP programer, not with the bootloader.

The programer _avr910_ is already referenced as desired programmer for the board. We have still to defines properties for th eprogrammer in the file _programmers.txt_

```
avr910.name=AVR ISP 910
avr910.communication=serial
avr910.protocol=avr910
avr910.speed=115200
```