#### 1/23/2024

Follow the tutorial [here](https://pimylifeup.com/raspberry-pi-gpio/) to enable GPIO and to get the script which grabs pin 7, and toggles it on and off. \

Note: Pin 7 is not GPIO7. \
Pin 7 is actually GPIO4. \
<br>

You can the circuit with PIN 1, which outputs 3.3v constantly.

script included below

```
#import the GPIO and time package
import RPi.GPIO as GPIO
import time
GPIO.setmode(GPIO.BOARD)
GPIO.setup(7, GPIO.OUT)
# loop through 50 times, on/off for 1 second
for i in range(50):
    GPIO.output(7,True)
    time.sleep(1)
    GPIO.output(7,False)
    time.sleep(1)
GPIO.cleanup()
```

The Raspberry PI version I am using: \
Raspberry Pi 3 Model B+ \
2017

[Video Notes](https://youtu.be/5gdS-ftyAyo)

Resources:

- [Enable GPIO on Pi] (https://pimylifeup.com/raspberry-pi-gpio/)
- [Enable Ic2 on Pi] (https://pimylifeup.com/raspberry-pi-i2c/)
- [Diagram of GPIO pins] (./GPIO-Pintout-diagram-v2.pdf)
- [Numbered diagram of pins] (https://techexplorations.com/guides/rpi/begin/raspberry-pi-pins-gpio/)
- [breadboard usage] (https://www.sciencebuddies.org/science-fair-projects/references/how-to-use-a-breadboardb)
