# Installing & Configuring Raspberry Pi Computers

## Tasks

1. Install OS image
1. Enable serial console  
   Add the following lines near the end of `config.txt` in the root of the boot volumne on the SD card:
   ```
   # Enable serial console
   enable_uart=1
   ```
1. [Configure WiFi network](network.md)
1. Enable SSH
1. Set hostname
1. Set password

## Manual / Standard Method

## Pi Bakery

## Serial Console

Using an Adafruit USB-to-Serial cable, connect:
* Black to GND (pin 3 on outside from near edge)
* White to TXD (pin 4 on outside)
* Green to RDX (pin 5 on outside)
* Red unconnected (except on Pi 0 where it can be used to supply power through the 5V pin (1 or 2)

The default baud rate is 115,200

Connect with `screen /dev/cu.usbserial-NNNN 115200`.
