# my Robot

> A generic home world with multiple obstacles and  differential-drive robot.

This is a generic appartment world loaded with obstacles. It includes a  differential drive robot equipped with a  Hokuyo lidar and a camera (800x800 pixels). Robot Model is created via xacro. This repo can be used as reference for creating simple robots via xacro.  World also incudes a small white sphere that can be used to make the robot move by using the [ball chaser](https://github.com/lemontyc/ball_chaser) repository.

## Requirements

* ROS Kinetic or up.
* Gazebo 7.16.0 or up.

## Running

1. Source your environment.
2. Run the **world.launch** file:
```sh
$ roslaunch my_robot world.launch
```
3. Open **config.rviz** in RVIZ to visualize lidar point cloud and camera image.
4. Move the robot by publishing  a **/Twist** message to topic **/cmd_vel**:
```sh
$ rostopic pub /cmd_vel geotry_msgs/Twist "linear:
  x: 0.3
  y: 0.0
  z: 0.0
angular:
  x: 0.0
  y: 0.0
  z: 0.0"
```

This will start gazebo with the world loaded, as well as RVIZ. If you publish a message, the robot will move.

## Pictures

#### World
![World](images/world.png)

#### Robot
![World](images/robot.png)

## Meta

* **Luis M.**           - [GitHub](https://github.com/lemontyc)

Distriuted under the MIT License. See ``LICENSE`` for more information.

This project was developed for the **Robotics software Engineer Nanodegree Program** course at **Udacity**.