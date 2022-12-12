# Wiegand Raspberry Pi
Read 26 bit Wiegand data (from two I/O data lines) and output the result.

### Output
```
Read 26 bits: 0|0000|0000|0000|1111|0001|1111|0
Hex: 1E3E
Facilty: 0
Code: 3871

Read 26 bits: 0|0000|0000|0000|1111|0001|1101|1
Hex: 1E3B
Facilty: 0
Code: 3869
````

### Requirements
#### Hardware
* Raspberry Pi (Pi 4)
* 5v to 3v level shifter (SN74LVC245)
* Wiegand device (Essex Electronics Wiegand Keypad/Prox Reader (T-Prox Series) TPX-26I)

#### Software
* The latest Raspberry Pi Software Raspian from https://www.raspberrypi.com/software/
* The latest WiringPI from https://github.com/WiringPi/WiringPi

### Build
After compiling WiringPi

Compile wiegand-raspberrypi.c
````
$ gcc -owiegand-raspberrypi wiegand-raspberrypi.c -lwiringPi -lpthread -lrt
$ ./wiegand-raspberrypi
````
