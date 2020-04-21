# GPIO Lore

## 1-Wire Bus
* Default GPIO pin is #4.
* A 4.7K Ω pullup to the 3.3V rail is required.
* The default can be changed by editing `/boot/config.txt` to add: `dtoverlay=w1-gpio,gpiopin=N` where N is the desired GPIO pin. Whitespace is not allowed.
* Multiple 1-Wire busses are supported in recent kernels (discussion [here](https://www.raspberrypi.org/forums/viewtopic.php?t=156734).
* [Additional info](https://pinout.xyz/pinout/1_wire).
