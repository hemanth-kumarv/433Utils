# About 433Kit

433Kit is a collection of code and documentation designed to assist you in the connection and usage of RF 433MHz transmit and receive modules to/with your Arduino and Rapberry Pi.

It consists of two main sections- Arduino sketches and Raspberry Pi command line utilities.  You'll find those in appropriately named folders.

## Requirements

1. An Arduino (two is ideal)
2. A Raspberry Pi
3. the git commandline tool, on both your Arduino IDE machine and your RPi

## Installation

### Arduino Sketches

Place the Sketches in your normal Arduino Sketches location.  Install any required libraries:

1. TODO servo lib url
2. [rc_switch](http://code.google.com/p/rc-switch/)

### RPi\_utils

From your RPi, clone this archive:

1. git clone git@github.com:justy/433Kit.git

2. cd i433Kit/RPi\_utils

3. (As per the original rc_switch distribution) you have to install the [wiringpi](https://projects.drogon.net/raspberry-pi/wiringpi/download-and-install/) library.
After that you can compile the example programs by executing *make*. 

## Usage

### send 
```sudo ./send systemCode unitCode command```

This command is unaltered from the original rc\_switch distribution.


### codesend 
```sudo ./codesend decimalcode```

This command uses a single Ninja Blocks compatible decimal code.  Sniff out codes using the RF\_Sniffer.ino Arduino sketch, included in this distribution.

You can use codesend to control the wireless servo on your Arduino.
(The sketch is Servo\_Receive\_Demo.ino)

I've implemented the most bare-bones of controls here.  Try:

```sudo ./codesend 500000 # to move the servo up```

```sudo ./codesend 500001 # to move the servo down```

```sudo ./codesend 500002 # to move the servo left```

```sudo ./codesend 500003 # to move the servo right```

```sudo ./codesend 500004 # to move the servo home```
