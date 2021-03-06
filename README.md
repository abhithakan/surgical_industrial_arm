# Attaching a Surgical Insertion Tool onto the End-effector of an Industrial Robot

## Contents

This repository contains packages used to drive an ABB robot (can be replaced by other robots) and an insertion tool for da Vinci Surgical System controlled by four servos. The software structure is shown in the following figure.

## Dependency 
* [ROS-industrial/abb_experimental]
* [wpi-dvrk-ros]
* [Modern_Robotics]
* [pyquaternion]


## Install
* Install ```abb_experimental``` from <https://github.com/wangyanhit/abb_experimental>

* Clone this package in (ROS workspace path)/src folder
```
git clone https://github.com/wangyanhit/surgical_industrial_arm.git
```

* Clone dvrk-ros in (ROS workspace path)/src folder (this package includes the model of the insertion tool)
```
git clone https://github.com/WPI-AIM/dvrk_env.git
```


## Usage
* launch ABB Gazebo model
```
roslaunch abb_irb120_gazebo irb120_gazebo.launch
```

* run package node
```
rosrun surgical_industrial_arm trajectory_generator.py
```

[Modern_Robotics]: http://hades.mech.northwestern.edu/index.php/Modern_Robotics
[wpi-dvrk-ros]: https://github.com/WPI-AIM/dvrk_env
[ROS-industrial/abb_experimental]: https://github.com/ros-industrial/abb_experimental
[pyquaternion]: http://kieranwynn.github.io/pyquaternion/