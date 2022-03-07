# Make robut move on ROS simulation by ps3 controller 

```ps3_joy_msgs``` is original Msg to control robut by ps3 controller.

with "ps3_joy_basic", you can control turtlebot by ps3 controller
```zsh
$ roslaunch ps3_joy_basic turtle.launch
```



with "ps3_rviz_move", you can control custmize your robut on Rviz by ps3 controller
```zsh
$ roslaunch ps3_rviz_move movement_robot.launch joy:=true
```

