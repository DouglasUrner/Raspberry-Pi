# Raspberry Pi Networking

## Configuring for headless boot

1. Install OS image on an SD card.
1. Touch `ssh` in the root of the `boot` volume.
1. Configure wifi (if using):

```
```
1. Move the SD card to the Pi and boot.
1. `ssh pi@raspberrypi.local # default password is 'raspberry'`

## MAC Address – Finding a Pi on your network

All Raspberry Pi MAC addresses start with `B8:27:EB`, you can find their IP addresses with ARP:

```bash
arp -an | grep -i 'B8:27:EB'
```
