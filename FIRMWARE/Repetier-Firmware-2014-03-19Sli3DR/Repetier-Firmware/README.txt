Compilation instructions

1.  Install Arduino IDE
    You get the latest Arduino IDE here:
    http://arduino.cc/en/Main/Software

    You need at least 1.0 for the Atmel AVR based boards and 1.5 for the ARM based boards like the due.

2.  Make sure the serial driver for your printer board is installed. The Arduino IDE contains signed drivers
    for the Arduino boards. Depending on your board you might need different drivers then these. For Linux and Mac
    you often do not need any additional drivers. Ask your printer/board vendor which driver you need,
    if that is not clear to you.

3.  Some boards that are not original arduino boards and not 100% compatible to them, need separate extensions
    to the Arduino IDE. Install them.

4.  Start Arduino IDE and open the file "Repetier.ino"

5.  Select the board and port for upload in the arduino ide.

6.  Check Configuration.h for hints, if something needs to be checked or modified.

7.  Upload the firmware with the upload button (right arrow in toolbar).

If you have a normal mega 2560 compatible board, you can use codeblocks for arduino instead of the arduino ide:
http://arduinodev.com/codeblocks/
Open the Repetier.cbp file instead of the ino file and start with 6.

HINT: It you have enabled eeprom support, the first upload will copy the configurations into the eeprom. Later
uploads will NOT overwrite these settings! Connect with Repetier-Host to your printer and open the eeprom editor
to change these values. Alternatively, send the commands
 M502
 M500
to copy the new values in Configuration.h to eeprom.
