# `Simple ADC on the Tiva-C TM4C123x`

This is a simple C program for the Tiva-C TM4C123x evaluation board. It runs the ADC on pin AIN1/PE2 and displays the
raw samples on its USART. On the eval board the target µC usart is passed via the debugging µC to the computer as an USB
serial (/dev/ttyACM0).

The goal of this program is to investigate sampling of low milivolt voltages…

# Quick start:

``` console
$ cd src/
$ make
$ lm4flash gcc/main.bin
$ picocom /dev/ttyACM0 -b 115200
```

# Required tools:

* arm-none-eabi-gcc/binutils
* [lm4flash](https://github.com/utzig/lm4tools)

# References:

Most of the supporting libs are taken from https://github.com/yuvadm/tiva-c. That includes:
* driverlib/
* inc/
* utils/
* makedefs

The ADC code is adapted from https://github.com/LuisAfonso95/TM4C123-Launchpad-Examples/tree/master/ADC%20-%20Temp%20sensor
