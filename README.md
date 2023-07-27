# MobileRobot-Openloopcontrol
## Aim:

To develop a python control code to move the mobilerobot along the predefined path.

## Equipments Required:
1. RoboMaster EP core
2. Python 3.7

## Procedure

Step1:

Define the predefined path
Create a list or array to store the coordinates of the robot's predefined path.
Each coordinate should represent a point along the path that the robot needs to follow.

Step2:

Initialize the robot's starting position
Set the robot's initial position to the first coordinate in the predefined path.

Step3:

Move the robot along the path
Loop through each coordinate in the predefined path, starting from the second coordinate.
Calculate the distance and direction from the robot's current position to the next coordinate.
Use appropriate robot control commands to move the robot towards the next coordinate.
Repeat this process for each coordinate in the predefined path.

Step4:

Check if the robot has reached the end of the path
After completing the loop, compare the robot's final position with the last coordinate in the
predefined path.
If the two positions match or are within a certain threshold, the robot has successfully reached
the end of the path.
If not, modify the path or make other adjustments as needed.

Step5:
End the program

Once the robot has reached the end of the path, stop the program or execute any additional
tasks required.
Print a message or perform any necessary cleanup steps before terminating the program.


## Program
```
#To develop a python control code to move the mobilerobot along the predefined path.
#Developed by :MIDHUN S
#Reference no :23003250

from robomaster import robot
import time
from robomaster import camera

if _name_ == '_main_':
    ep_robot = robot.Robot()
    ep_robot.initialize(conn_type="ap")

    ep_chassis = ep_robot.chassis
    ep_led = ep_robot.led
    ep_camera = ep_robot.camera
    print("Video streaming started.....")
    ep_camera.start_video_stream(display=True, resolution = camera.STREAM_360P)
    ep_chassis.move(x =2.8,y=0,z=0,xy_speed=0.75).wait_for_completed()
    ep_led.set_led(comp="all",r=255,g=0,b=0,effect="on")
    ep_chassis.move(x =0,y=0,z=50,xy_speed=0.75).wait_for_completed()
    ep_led.set_led(comp="all",r=255,g=0,b=0,effect="on")
    ep_chassis.move(x =0.5,y=0,z=0,xy_speed=0.75).wait_for_completed()
    ep_led.set_led(comp="all",r=255,g=255,b=0,effect="on")
    ep_chassis.move(x =0,y=0,z=50,xy_speed=0.75).wait_for_completed()
    ep_led.set_led(comp="all",r=255,g=0,b=255,effect="on")
    ep_chassis.move(x =0.8,y=0,z=0,xy_speed=0.75).wait_for_completed()
    ep_led.set_led(comp="all",r=128,g=128,b=0,effect="on")
    ep_chassis.move(x =0,y=0,z=80,xy_speed=0.75).wait_for_completed()
    ep_led.set_led(comp="all",r=255,g=255,b=0,effect="on")
    ep_chassis.move(x =1.4,y=0,z=0,xy_speed=0.75).wait_for_completed()
    ep_led.set_led(comp="all",r=128,g=255,b=0,effect="on")
    ep_chassis.move(x =0,y=0,z=-45,xy_speed=0.75).wait_for_completed()
    ep_led.set_led(comp="all",r=255,g=255,b=0,effect="on")
    ep_chassis.move(x =1.5,y=0,z=0,xy_speed=0.75).wait_for_completed()
    ep_led.set_led(comp="all",r=0,g=0,b=0,effect="on")
    ep_chassis.move(x =0,y=0,z=45,xy_speed=0.75).wait_for_completed()
    ep_led.set_led(comp="all",r=255,g=128,b=0,effect="on")
    ep_chassis.move(x =1.5,y=0,z=0,xy_speed=0.75).wait_for_completed()
    ep_led.set_led(comp="all",r=255,g=255,b=255,effect="on")
    ep_chassis.move(x =0,y=-0.3,z=0,xy_speed=0.75).wait_for_completed()
    ep_led.set_led(comp="all",r=0,g=255,b=0,effect="on")
    ep_chassis.move(x =0,y=0,z=95,xy_speed=0.75).wait_for_completed()
    ep_led.set_led(comp="all",r=255,g=0,b=255,effect="on")
    ep_chassis.move(x =1.7,y=0,z=0,xy_speed=0.75).wait_for_completed()
    ep_led.set_led(comp="all",r=255,g=255,b=0,effect="on")
    ep_chassis.move(x =0,y=0,z=70,xy_speed=0.75).wait_for_completed()
    ep_led.set_led(comp="all",r=255,g=255,b=0,effect="on")
    ep_chassis.move(x =0.7,y=0,z=0,xy_speed=0.75).wait_for_completed()
    ep_led.set_led(comp="all",r=0,g=0,b=255,effect="on") 
    ep_chassis.move(x =0,y=0,z=20,xy_speed=0.75).wait_for_completed()
    ep_led.set_led(comp="all",r=0,g=255,b=0,effect="on") 
    time.sleep(4)
    ep_camera.stop_video_stream()
    print("Stopped video streaming.....")
    ep_robot.close()
```

## MobileRobot Movement Image:

![robo](./img/robomaster.png)

![robo](/Screenshot%202023-07-26%20224353.jpg)

## MobileRobot Movement Video:


[![IMAGE ALT TEXT HERE](https://img.youtube.com/vi/YOUTUBE_VIDEO_ID_HERE/0.jpg)](https://www.youtube.com/watch?v=YOUTUBE_VIDEO_ID_HERE)

https://youtu.be/2N9vcPVlHMU

## Result:
Thus the python program code is developed to move the mobilerobot in the predefined path.

```
Mobile Robotics Laboratory
Department of Artificial Intelligence and Data Science/ Machine Learning
Saveetha Engineering College
```
