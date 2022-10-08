# FlipperZero-CONVERT / Wifi Board / DEAUTH V2.0 - ESP8266 for Flipper Zero (Deauth working)



- Many users in the Flipper Zero community have found that using the <a href="https://github.com/SequoiaSan/FlipperZero-Wifi-ESP8266-Deauther-Module">SequoiaSan</a> tool V1, the Deauth does not work,
here you can find the optimized Version 2 of the <a href="https://github.com/SequoiaSan/FlipperZero-Wifi-ESP8266-Deauther-Module">original Deauther</a> tool already compiled (.faps) and working for the Flipper Zero plus How-To and more.

# How-TO Flash the Deauther V2-6-0 .bin for the Esp8266 board

- Download the official .bin of the Deauther V2.6.0 tool from <a href="https://github.com/HEX0DAYS/FlipperZero-CONVERT/blob/96a9ca4bcb4e93c22d117a1ad27422149cdea6fb/Deauther2.6.0_FZ/esp8266_deauther_2.6.0.bin">HERE</a> , you can use the <a href="https://github.com/SpacehuhnTech/esp8266_deauther/wiki/Installation/70c7169963788c6a00cba1aa5d1939aedd463567#compiling-using-arduino-ide">ArduinoIDE</a> ,<a href="https://github.com/SpacehuhnTech/esp8266_deauther/wiki/Installation/70c7169963788c6a00cba1aa5d1939aedd463567#esptool-gui">Esptool-gui</a> ,Esptool or <a href="https://github.com/SpacehuhnTech/esp8266_deauther/wiki/Installation/70c7169963788c6a00cba1aa5d1939aedd463567)">many others</a> ,below I will show you how to do it with Esptool which is very easy and fast. 
# How-TO Flash the Deauther V2.6.0 .bin for the Esp8266 board using ESPTOOL
After download the V2 Deauther .bin we need to flash it on the Esp8266 via a single command. Just plug the USB Cable from Esp8266 to Computer and then launch this command from Esptool.

- Using the NodeMCU (or any similar development board), the flash location is 0x0000 and the mode is dout.

<b>esptool.py -p /dev/ttyUSB0 write_flash -fm dout 0x0000 esp8266_deauther_2.6.0.bin</b> or 

<b>esptool -p /dev/ttyUSB0 write_flash -fm dout 0x0000 esp8266_deauther_2.6.0.bin</b>

Where /dev/ttyUSB0 is the COM port of your device, write_flash is telling the program to write to flash memory, -fm dout is the flash mode and esp8266_deauther_2.6.0.bin is the name of your .bin file. if you get an error with this command, just enter your serial port replaced to /dev/ttyUSB0 , you can use <a href="https://www.uwe-sieber.de/usbtreeview_e.html#download">UsbTreeView</a> for see all the serial ports are connected via USB, after you have your COM port, just replace /dev/ttyUSB0 with your COM port, Ex COM1, COM2, COM3, COM4, COM5. And then Launch the command and wait for the flashing end


