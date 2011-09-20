Arduino TextMate Bundle
=======================
[TextMate](http://macromates.com) is the best editor in human history. [Arduino](http://arduino.cc) is the easiest embedded platform to dive into. Why don't the two work together? The Arduino TextMate Bundle solves that glaring error, and the universe is thus balanced.

There are other TextMate bundles out there, but they're mostly over two years old and don't work with new Arduino versions. This project aims to remain up-to-date and make embedded as enjoyable as everything else in TextMate.

The little 'a' in '0.21a' stands for 'alpha'. Read that as "might not work for you". It will grow and improve with time, but for now brace yourself for bugs. That means bug reports, feature requests and patches!

As of 0.21a, the bundle can compiles and uploads to the device, provides access to the documentation and highlights syntax correctly.

Installation
============
1. [Get the latest Arduino](http://arduino.cc/en/Guide/MacOSX). 0018 and later is supported, and it must be installed to /Applications
2. [Get TextMate](http://macromates.com/).
3. [Get the latest Arduino TextMate bundle](https://github.com/nasser/arduino.tmbundle/zipball/master).
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
    <td>The serial port to upload from (defaults to <code>/dev/tty.usbserial-*</code>)</td>
  </tr>
  <tr>
    <td>ARDUINO_UPLOAD_RATE</td>
    <td>The baud rate to upload at (defaults to <code>57600</code>)</td>
  </tr>
  <tr>
    <td>ARDUINO_AVRDUDE_PROGRAMMER</td>
    <td>The programmer to use (defaults to <code>stk500v1</code>)</td>
  </tr>
  <tr>
    <td>ARDUINO_MCU</td>
    <td>The Atmel chip on the board (defaults to <code>atmega328p</code>)</td>
  </tr>
  <tr>
    <td>ARDUINO_F_CPU</td>
    <td>The clock speed of the Atmel chip (defaults to <code>16000000</code>)</td>
  </tr>
</table>

Todo
====
* Useful error messages (relative to the .pde file, not the generated .cpp file)

Bleeding Edge
=============
For the adventurous

    git clone git://github.com/nasser/arduino.tmbundle.git ~/Library/Application\ Support/TextMate/Bundles/Arduino.tmbundle
    
Changes
=======
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