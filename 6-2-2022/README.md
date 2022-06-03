Made master program with implemented code and gyro turn function
```python

from spike import PrimeHub, LightMatrix, Button, StatusLight, ForceSensor, MotionSensor, Speaker, ColorSensor, App, DistanceSensor, Motor, MotorPair
from spike.control import wait_for_seconds, wait_until, Timer
from math import *

hub = PrimeHub()
motor_pair = MotorPair('B', 'A') 

def gyroturn(degrees):
    if degrees.contains(-):
        d1 = -25
    else:
        d1 = 25
    while(hub.motion_sensor.get_yaw_angle() > degrees):
        motor_pair.start(-100, d1)
    motor_pair.stop()

i = 0
while True:
    hub.light_matrix.write(str(i))
    if hub.left_button.is_pressed():
        hub.status_light.on('blue')
        wait_for_seconds(1)
        hub.motion_sensor.reset_yaw_angle()
        wait_for_seconds(0.5)
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
