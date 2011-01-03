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

Usage
=====
* **⌘U** Compiles and uploads your sketch to the connected Arduino
* **⌃⌥⌘H** Opens up local HTML documentation on to current word
* **Bundles > Arduino > Watch Serial Port** Opens a terminal window monitoring the serial port.
* **File > New From Template > Arduino > Basic Sketch** Creates a file with a blank basic sketch.

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