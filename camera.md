# Raspberry Pi Camera Info

* https://magpi.raspberrypi.org/books/camera-guide

**Take a still on a headless Pi and copy it to the local machine:**  
```bash
ssh pi@pi0w-00.local -- raspistill -n -o - > /tmp/foo.jpg; open /tmp/foo.jpg
```
