# Raspberry Pi Networking

## Configuring for headless boot

1. Install OS image on an SD card.
   - 16 GD or larger, speed?
   - For embedded systems, use Raspbian Lite.
1. Touch `ssh` in the root of the `boot` volume.
1. Configure wifi (if using):  
   Create `wpa_supplicant.conf` in the root of the `boot` volume, and add the following content:
   ```
   country=COUNTRY
   ctrl_interface=DIR=/var/run/wpa_supplicant GROUP=netdev
   update_config=1
   network={
          ssid="SSID"
          psk="PASSWORD"
          key_mgmt=WPA-PSK
   }
   ```
   Where `COUNTRY` is the two letter code for your location, e.g., `US`. `SSID` and `PASSWORD` are what you'd expect.
1. Move the SD card to the Pi and boot.
1. `ssh pi@raspberrypi.local # default password is 'raspberry'`

## Finding a Pi on your network

On macOS: `ping raspberrypi.local` will do it, assuming the default configuration.

All Raspberry Pi MAC addresses start with `B8:27:EB`, you can find their IP addresses with ARP:

```bash
arp -an | grep -i 'B8:27:EB'
```
