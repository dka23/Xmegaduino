XmegaDuino
===========

Port of the Arduino IDE, core, libraries and bootloader to support the Atmel XMEGA family of chips.

Currently supported boards:

* AVR xplain board
* Akafuino X board
* Sparkfun xmega100 breakout board

The following boards should work with a little tweaking:

* Magnetovore
* Megavore
* Boston Android

This project has replaced the xmegaduino project on Google Code (http://code.google.com/p/xmegaduino/)
and has been active since September 2011. It supersedes the earlier xplainduino.

Installation
============

Download from [here](https://github.com/akafugu/Xmegaduino/downloads).

* Windows
* OS X
* Linux

Requirements
============

* AVR xplain board

The LUFA project provides a replacement USB firmware that can act as a PDI programmer.
You can also use a PDI programmer such as the AVR Dragon.

* [Sparkfun xmega100](http://www.sparkfun.com/products/9546)

Requires a PDI programmer, such as the AVR Dragon in order to upload sketches and burn bootloaders.

* [Akafuino X](http://www.akafugu.jp/posts/products/akafuino/)

Comes with a bootloader pre-installed and can be used directly from the Xmegaduino IDE.

Status
======

The Xmegaduino project is beta quality, and not all the features of the Arduino IDE are supported yet.

Working features:

* digitalRead and digitalWrite
* millis and delay
* micros and delayMicroseconds
* Serial on USB (USARTC0), Serial1 on pins D2/D3 (USARTD0) and Serial2 on D6/D7 (USARTD1).
* analogRead
* analogWrite
* attachInterrupt, detachInterrupt, interrupts, noInterrupts
* Upload using bootloader over usb port, D2/3, or D6/7.
* Burning bootloader from arduino IDE
* DAC (using xmDAC library)
* Wire
* shiftOut, shiftIn, pulseIn (not tested)
* tone
* SPI library
* EEPROM library

Todo:

* analogReference
* Ethernet library
* Servo library
* Stepper library

Changelog
=========

Beta4b (based on Arduino 1.0.1-rc2) (2012-04-19):

* Updated only for Mac OS X, removed dynamic dependencies on avr-gcc.

Beta4 (based on Arduino 1.0.1-rc2):

* New avr-gcc 4.5.1, avr-libc 1.7.1 for all platforms (Windows, Mac OS X, Linux 32/64)
* Linux now comes with bundled avr-gcc and avr-libc
* Use correct SPI port on Akafuino X (pin 10-13)
* Upload sketch to XPlain using PDI
* Translated to 23 different languages (Thanks to Arduino)

Beta3 (based on Arduino 1.0):

Big thanks goes out to Brendan Powers and Russell for their contributions 

* xmDAC now works again
* EEPROM library fixed
* All baud rates are now dynamically calculated
* SPI library ported
* shiftIn function implemented
* tone implemented using timer TCC1
* LEVEL interrupt mode
* Replicated Arduino's pullup behavior when writing to an input pin

