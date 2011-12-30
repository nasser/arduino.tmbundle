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
    <td>ARDUINO_PORT</td>
    <td>The serial port to upload from (defaults to <code>/dev/tty.usbmodem*</code>)</td>
  </tr>
  <tr>
    <td>ARDUINO_UPLOAD_RATE</td>
    <td>The baud rate to upload at (defaults to <code>115200</code>)</td>
  </tr>
  <tr>
    <td>ARDUINO_AVRDUDE_PROGRAMMER</td>
    <td>The programmer to use (defaults to <code>arduino</code>)</td>
  </tr>
  <tr>
    <td>ARDUINO_MCU</td>
    <td>The Atmel chip on the board (defaults to <code>atmega328p</code>)</td>
  </tr>
  <tr>
    <td>ARDUINO_F_CPU</td>
    <td>The clock speed of the Atmel chip (defaults to <code>16000000</code>)</td>
  </tr>
  <tr>
    <td>ARDUINO_VARIANT</td>
    <td>The Arduino variant being used. Can be one of <code>standard</code>, <code>micro</code>, <code>mega</code>, <code>leonardo</code>, or <code>eightanaloginputs</code>. (defaults to <code>standard</code>)</td>
  </tr>
</table>

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