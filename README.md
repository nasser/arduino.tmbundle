Arduino TextMate Bundle 1.0a
============================
[TextMate](http://macromates.com) is the best editor in human history. [Arduino](http://arduino.cc) is the easiest embedded platform to dive into. Why don't the two work together? The Arduino TextMate Bundle solves that glaring error, and the universe is thus balanced.

There are other TextMate bundles out there, but they're mostly over two years old and don't work with new Arduino versions. This project aims to remain up-to-date and make embedded as enjoyable as everything else in TextMate.

The little 'a' in '1.0a' stands for 'alpha'. Read that as "might not work for you". It will grow and improve with time, but for now brace yourself for bugs. That means bug reports, feature requests and patches!

As of 1.0a, the bundle can compiles and uploads to the device, provides access to the documentation and highlights syntax correctly.

Installation
============
1. [Get the latest Arduino](http://arduino.cc/en/Guide/MacOSX). Version 1.0 and later is supported, and it must be installed to /Applications
2. [Get TextMate](http://macromates.com/).
3. [Get the latest Arduino TextMate bundle](https://github.com/nasser/arduino.tmbundle/zipball/v1.0a).
4. Extract the zip file to `~/Library/Application Support/TextMate/Bundles/Arduino.tmbundle`
5. If TextMate was open during this process, click Bundles>Bundle Editor>Reload Bundles
6. Check the 'Default Environment vars' near the top of `~/Library/Application Support/TextMate/Bundles/Arduino.tmbundle/Support/Makefile`.  Any you need to override - especially check the ARDUINO_MCU var - can be added in TextMate's Preferences => Advanced => Shell Variables.


Usage
=====
* **⌘U** Compiles and uploads your sketch to the connected Arduino
* **⌃⌥⌘H** Opens up local HTML documentation on to current word
* **Bundles > Arduino > Watch Serial Port** Opens a terminal window monitoring the serial port.
* **File > New From Template > Arduino > Basic Sketch** Creates a file with a blank basic sketch.

Shell Variables
===============
The compile/upload process can be finely controlled using TextMate's shell variables.

Textmate > Preferences > Advanced > Shell Variables

<table>
  <tr>
    <th>Variable</th>
    <th>Value</th>
  </tr>
  <tr>
    <td>BOARD</td>
    <td>The Arduino variant being used. See table below.</td>
  </tr>
  <tr>
	  <td>SERIALDEV</td>
	  <td>We try to guess the correct serial port. If that is not possible, you have to set the correct serial port. <br />Like: <code>/dev/tty.usbmodem1411</code></td>
  </tr>
</table>

Supported Arduino Boards
========================
Value | Description 
------|------------
uno          |Arduino Uno
atmega328    |Arduino Duemilanove w/ ATmega328
diecimila    |Arduino Diecimila or Duemilanove w/ ATmega168
nano328      |Arduino Nano w/ ATmega328
nano         |Arduino Nano w/ ATmega168
mega2560     |Arduino Mega 2560 or Mega ADK
mega         |Arduino Mega (ATmega1280)
leonardo     |Arduino Leonardo
esplora      |Arduino Esplora
micro        |Arduino Micro
mini328      |Arduino Mini w/ ATmega328
mini         |Arduino Mini w/ ATmega168
ethernet     |Arduino Ethernet
fio          |Arduino Fio
bt328        |Arduino BT w/ ATmega328
bt           |Arduino BT w/ ATmega168
LilyPadUSB   |LilyPad Arduino USB
lilypad328   |LilyPad Arduino w/ ATmega328
lilypad      |LilyPad Arduino w/ ATmega168
pro5v328     |Arduino Pro or Pro Mini (5V, 16 MHz) w/ ATmega328
pro5v        |Arduino Pro or Pro Mini (5V, 16 MHz) w/ ATmega168
pro328       |Arduino Pro or Pro Mini (3.3V, 8 MHz) w/ ATmega328
pro          |Arduino Pro or Pro Mini (3.3V, 8 MHz) w/ ATmega168
atmega168    |Arduino NG or older w/ ATmega168
atmega8      |Arduino NG or older w/ ATmega8
robotControl |Arduino Robot Control
robotMotor   |Arduino Robot Motor

Bleeding Edge
=============
For the adventurous

    git clone git://github.com/nasser/arduino.tmbundle.git ~/Library/Application\ Support/TextMate/Bundles/Arduino.tmbundle
    
Changes
=======
1.0a
----
* Fixed for Arduino 1.0
* Improved local help command
* Changed versioning scheme to match Arduino's. This bundle's version will always be equal to the version of Arduino it is most compatible with.

0.21a
----
* Added snippets for common methods
* Added an Arduino project template
* Altered the monitor script - it's now aware of your USB ports

0.2a
----
* Compile/upload bug fixed
* Syntax highlighting added
* Local help added
* Initial Watch Serial Port implementation
* More intelligent Makefile with environment variable overrides

0.1a
----
* Initial release, basic implementation of compiling/uploading