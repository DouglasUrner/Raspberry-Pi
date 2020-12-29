# Installing & Configuring Raspberry Pi Computers

## Generating SSH Keys

[Generating a new SSH key and adding it to the ssh-agent](https://docs.github.com/en/free-pro-team@latest/github/authenticating-to-github/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)

## Tasks

Depending on the method chosen for building the SD image some steps may have to be done after the first boot.

1. Install OS image
1. Enable serial console  
   Add the following lines near the end of `config.txt` in the root of the boot volumne on the SD card:
   ```bash
   # Enable serial console
   enable_uart=1
   ```
1. [Configure WiFi network](networking.md)
1. Enable SSH
1. Set hostname
1. Set timezone
   ```bash
   sudo timedatectl set-timezone America/Vancouver
   ```
1. Change password
1. Install `pip`
1. Enable interfaces

## NixOS

[NixOS](https://nixos.org)

## Manual / Standard Method

1. Install the OS image (using [Raspberry Pi Imager](https://www.raspberrypi.org/downloads/))
1. Remount the SD card
1. Enable ssh: `touch /Volumes/boot/ssh`
1. Create [`wpa_suplicant.conf`](networking.md) and set the network configuration.
1. Enable the serial console
1. Enable GPIO interfaces
   - [1-Wire](gpio.md): `dtoverlay=w1-gpio,gpiopin=4`
1. Unmount the SD card
1. Install in the Pi and boot
1. Connect to the Pi: `ssh pi@raspberrypi.local`

## Pi Bakery

## Serial Console Connections

Using an Adafruit USB-to-Serial cable, connect:
* Black to GND (pin 6 - 3rd on outside (closest to edges)
* White to TXD (pin 8 - 4th on outside)
* Green to RDX (pin 10 - 5th on outside)
* Red unconnected (except on Pi 0 where it can be used to supply power through the 5V pin (1 or 2)

The default baud rate is 115,200

Connect with `screen /dev/cu.usbserial-NNNN 115200`.

### Enabling the serial console after first boot
