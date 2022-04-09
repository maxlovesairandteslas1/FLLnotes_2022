# For Tomorrow
Need to do: 
### Color sensor
test color sensor: ambient light, accuracy. \
Also need to test how the color reacts in different situations, like with a high base or low base, in the light or shaded. \
We also need to work on gyro, see different measurements. 

### Line follow notes
shouldn't be too hard, python is very straightforward, so translating it from python should be no problem (PID is a different story tho... I was talking about zig-zag strategy).

### accel deccel
harder, but use math functions to translate.


## Notes about master program: 
there cannot be a master program, but like below, we can use the numbers to differentiate the mission runs, so it will be easier 

<img width="1440" alt="Screen Shot 2022-04-08 at 3 05 23 PM" src="https://user-images.githubusercontent.com/77656052/162538196-94e63c5d-c3c2-41b3-bd9d-6e853ea17d9d.png">
Alternitivly, we can use the left button as run, and iterate throught the programs with the right button \n
Example:


```python
from spike import PrimeHub, LightMatrix, Button, StatusLight, ForceSensor, MotionSensor, Speaker, ColorSensor, App, DistanceSensor, Motor, MotorPair
from spike.control import wait_for_seconds, wait_until, Timer
from math import *

hub = PrimeHub()
i = 0
while True:
    hub.light_matrix.write(str(i)) 
    if hub.left_button.is_pressed():
        hub.status_light.on('blue')
        wait_for_seconds(1.5)
        hub.light_matrix.off()
        if i = 0:
            # sample program
        elif i = 1:
            # sample program
        elif i = 2:
            # sample program
        elif i = 3:
            # sample program
        elif i = 4:
            # sample program
        elif i = 5:
            # sample program
        
    if hub.right_button.is_pressed():
        i = i + 1 
        if i > 6: # Can change 6 to the amout of programs - 1
            i = 0
```
Python is not that hard, but it needs a lot of getting used to, and logic, and familiarity of the functions and what do they do exactly

weeee

Made with ❤️ by max 

have a good day
