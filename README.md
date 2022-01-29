# Mobile-Robot



ROS (Robot Operating System)-based mobile robot is designed which uses “teleop_twist_keyboard” package to teleoperate the robot with keyboard.

"teleop_twist_keyboard" node publishes the messeges of "geometry_msgs" of type "Twist.msg" on topic "/cmd_vel " .

ESP32 is used in this project which subscribes to the topic "/cmd_vel " through “/rosserial_server" package.

A callbackfunction of the subscriber which receives "Twist" messages having the linear and angular velocities are converted to motor left and right velocities using differential drive kinematics and then mapped to respective pwm signals.

These signals are sent to motor drivers to drive the two motors accordingly.






Hardware Specifications: -


*RMCS-2303 DC Geared Motors

*BTS7960 Motor Drivers

*ESP32 Micro controller





![alt text](https://github.com/pranavpeddi1/Mobile-Robot/blob/main/Motors.jpg)

Motors with Motor Drivers and ESP32 

![alt text](https://github.com/pranavpeddi1/Mobile-Robot/blob/main/Mobile_RobotGiff.gif)
