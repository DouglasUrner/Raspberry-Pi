# Installing & Configuring Raspberry Pi Computers

## Tasks

Depending on the method chosen for building the SD image some steps may have to be done after the first boot.

1. Install OS image
1. Enable serial console  
   Add the following lines near the end of `config.txt` in the root of the boot volumne on the SD card:
   ```
   # Enable serial console
   enable_uart=1
   ```
1. [Configure WiFi network](networking.md)
1. Enable SSH
1. Set hostname
1. Set timezone
   ```bash
   sudo timedatectl set-timezone Australia/Sydney
   ```
1. Change password
1. Install `pip`
1. Enable interfaces

## Manual / Standard Method

1. Install the OS image (using[Raspberry Pi Imager](https://www.raspberrypi.org/downloads/))

## Pi Bakery

## Serial Console Connections

Using an Adafruit USB-to-Serial cable, connect:
* Black to GND (pin 3 on outside from near edge)
* White to TXD (pin 4 on outside)
* Green to RDX (pin 5 on outside)
* Red unconnected (except on Pi 0 where it can be used to supply power through the 5V pin (1 or 2)

The default baud rate is 115,200

Connect with `screen /dev/cu.usbserial-NNNN 115200`.
