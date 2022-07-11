```python
def accelDecel(fixSpeed,angle,initSpeed,endSpeed,change,useDegrees,degrees,brake):
    power = initSpeed]
    delta1 = motor1.get_degrees_counted()
    delta2 = motor2.get_degrees_counted()
    while !(power - 5 > endSpeed and power + 5 < endSpeed):
        power += change
        motor_pair.start(steering=(hub.motion_sensor.get_yaw_angle() - angle)*fixSpeed,power)
        wait_for_seconds(0.01)
    avg = (motor1.get_degrees_counted - delta1 + motor2.get_degrees_counted - delta2) / 2
    while !(!useDegrees or (avg - 10 < degrees and avg + 10 > degrees)):
        avg = (motor1.get_degrees_counted - delta1 + motor2.get_degrees_counted - delta2) / 2
        motor_pair.start(steering=(hub.motion_sensor.get_yaw_angle() - angle)*fixSpeed,power)
    if brake:
        motor_pair.stop()
        
```
this is very useful because it is
