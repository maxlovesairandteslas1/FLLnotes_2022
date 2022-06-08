# making a master program

I thought that we had to have a master program, so i thought of many different ways. \
imma make some pseudocode to show you what i mean
``` 
i = 1
run 1:
  function
run 2:
  function
run 3:
  function
while true:
  show the run number on screen
  if left button is pressed: (run program)
    if i = 1:
      run1()
    if i = 2:
      run2()
    if i = 3:
      run3()
  if right button is pressed:
    if i = 3:
      i=1
    else:
      i=i+1
    
```
now i make the code, here i go!

```python
from spike import PrimeHub, LightMatrix, Button, StatusLight, ForceSensor, MotionSensor, Speaker, ColorSensor, App, DistanceSensor, Motor, MotorPair
from spike.control import wait_for_seconds, wait_until, Timer
from math import *

hub = PrimeHub()
i = 1
def show1():
    hub.light_matrix.set_pixel(3, 5)
    hub.light_matrix.set_pixel(7, 5)
    hub.light_matrix.set_pixel(8, 5)
    hub.light_matrix.set_pixel(13, 5)
    hub.light_matrix.set_pixel(18, 5)
    hub.light_matrix.set_pixel(22, 5)
    hub.light_matrix.set_pixel(23, 5)
    hub.light_matrix.set_pixel(24, 5)
def show2():
    hub.light_matrix.set_pixel(2, 5)
    hub.light_matrix.set_pixel(3, 5)
    hub.light_matrix.set_pixel(4, 5)
    hub.light_matrix.set_pixel(9, 5)
    hub.light_matrix.set_pixel(12, 5)
    hub.light_matrix.set_pixel(13, 5)
    hub.light_matrix.set_pixel(14, 5)
    hub.light_matrix.set_pixel(17, 5)
    hub.light_matrix.set_pixel(22, 5)
    hub.light_matrix.set_pixel(23, 5)
    hub.light_matrix.set_pixel(24, 5)
def show3():
  hub.light_matrix.set_pixel(2, 5)
  hub.light_matrix.set_pixel(3, 5)
  hub.light_matrix.set_pixel(4, 5)
  hub.light_matrix.set_pixel(9, 5)
  hub.light_matrix.set_pixel(12, 5)
  hub.light_matrix.set_pixel(13, 5)
  hub.light_matrix.set_pixel(14, 5)
  hub.light_matrix.set_pixel(19, 5)
  hub.light_matrix.set_pixel(22, 5)
  hub.light_matrix.set_pixel(23, 5)
  hub.light_matrix.set_pixel(24, 5)

def determineshow():
  if i = 1:
      show1()
  if i = 2:
      show2()
  if i = 3:
      show3()

def run1():
    pass
def run2():
    pass
def run3():
    pass

def determinerun():
  if i = 1:
      run1()
  if i = 2:
      run2()
  if i = 3:
      run3()
while True:
    determineshow()
    if hub.left_button.is_pressed():
      hub.light_matrix.off()
      determinerun()
    if hub.right_button.is_pressed():
      if i>3:
          i = 1
      else:
          i = i+1


```
at the first, I made functions to put the numbers on the screen, so when i called the function, the number would show up. \
for the functions run1, run2, and run3, there are used to put the runs inside, so it is easier to edit

thanks
