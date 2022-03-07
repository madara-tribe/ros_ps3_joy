# Make robut move on ROS simulation by ps3 controller 

```ps3_joy_msgs``` is original Msg to control robut by ps3 controller.


# PS3 controller and button
If ps3 controller is connected, check by this command
```zsh
$ ls -l /dev/input/js*
### crw-rw-r--+ 1 root input 13, 0  7 13:53 /dev/input/js0
```
<img src="https://user-images.githubusercontent.com/48679574/157031297-c4567f7e-a34d-41c8-96e0-379c7db03609.jpg" width="300px"><img src="https://user-images.githubusercontent.com/48679574/157031307-7d2ce401-13d0-4443-b7cd-793df5a549e8.jpg" width="300px"><img src="https://user-images.githubusercontent.com/48679574/157031310-ef4a8f19-431d-44e5-b156-8f7663c93d63.jpg" width="300px">



## PS3 controller movement check.
```zsh
# After push PS button
$ roscore
$ rosrun joy joy_node
### [ WARN] [1646630772.708410626]: Couldn't set gain on joystick force feedback: Bad file descriptor
### [ INFO] [1646630772.710396915]: Opened joystick: /dev/input/js0 (Sony PLAYSTATION(R)3 Controller). deadzone_: 0.050000

$rostopic echo /joy
```


## requirements package
```zsh
sudo apt-get install ros-noetic-joy ros-noetic-teleop-twist-joy
#sudo apt-get install ros-noetic-joystick-drivers
```


# Performance

with "ps3_joy_basic", you can control turtlebot by ps3 controller
```zsh
$ roslaunch ps3_joy_basic turtle.launch
```

<img src="https://user-images.githubusercontent.com/48679574/157000034-c1490365-5c96-42ce-af54-d113b6c5c5be.png" width="500px">



with "ps3_rviz_move", you can control custmize your robut on Rviz by ps3 controller
```zsh
$ roslaunch ps3_rviz_move movement_robot.launch joy:=true
```

<img src="https://user-images.githubusercontent.com/48679574/157000012-3bf8fec2-4033-489b-a876-524f8819d67e.png" width="500px">

# References
・[ros_lecture](https://github.com/project-srs/ros_lecture)
・[ROS.org-ps3joy](http://wiki.ros.org/ps3joy)
・[ROS講座10 カスタムROSメッセージ](https://qiita.com/srs/items/7ac023c549e585caeed0)
