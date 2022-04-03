Observations for April 3rd, 2022:
in motor pairs, there is a thing called move_tank.
Move_tank moves the wheels, and each wheel can move independent speed. For example, the left wheel can move at 60 speed, while the right wheel can move at 75 speed.

Sample code for move_tank:
```python
from spike import MotorPair

motor_pair = MotorPair('B', 'A')
motor_pair.move_tank(10, 'cm', left_speed=25, right_speed=75)
```
distance format is either using inches or centimeters.
