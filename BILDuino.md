# BILDuino #
## The name ##
**BILD**' (german) - picture

'**Bildung**' (german) - education

'**arduino** - citation from www.arduino.cc:
> Arduino is an open-source electronics prototyping platform based on flexible, easy-to-use
> hardware  and software. It's intended for artists, designers, hobbyists, and anyone interested in creating
> interactive objects or environments.

With my words, the best things after sliced bread ;-)

## Project description ##
### Purpose and scope ###
The purpose of the BILDuino is to create a hardware module with acompanion software libraries for easy creation of simple devices with small graphics display, 8 buttons a simple user interface.
The module will commmunicate with other device with i2c, SPI and RS232.

Despite HW already exists (PCBs are already in small count manufactured and displays are here) for a longer time and has been working in more projects for more years, we desided to put peaces
together and trying to make a develelopment of a new devices quicker and easier also for others.

### Functions, data facts ###
#### HW ####
  * big ATMEGA32(644) DIL packaged
  * 2 I2C connectors
  * 1 RS232 with TTL
  * 128x64 graphical display
  * 8 buttons
#### SW ####
  * after small modification should run with stock arduino software
  * arduino core library
  * hardware independent display driver architecture (so display with driver could be easy replaced)
  * basic graphics core library (line, circles, texts)
  * basic UI (windows, frames, edit for various data types)
  * keys handling