# GPIO Lore

## 1-Wire Bus
* Default GPIO pin is #4.
* The default can be changed by editing `/boot/config.txt` to add: `dtoverlay=w1-gpio,gpiopin=N` where N is the desired GPIO pin. Whitespace is not allowed.
* Are multilpe 1-Wire busses supported?
