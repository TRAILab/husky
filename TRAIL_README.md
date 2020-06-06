TRAIL husky
===========

Modifications to the original Clearpath Husky code to support the addition of an AprilTag target on top of the Husky.

## Installation
1. Install ROS Kinetic (if not installed)

2. Create a catkin workspace (if one does not already exist)
```
mkdir -p ~/catkin_ws/src
cd ~/catkin_ws/src
catkin_init_workspace
```

3. Install dependencies
```
sudo apt update
sudo apt install ros-kinetic-husky-desktop ros-kinetic-husky-simulator
```

4. Clone this repository into the `src` folder

5. Check out the `kinetic-devel` branch

6. Build the package and source the catkin workspace
```
catkin build
source ~/catkin_ws/devel/setup.bash
```

7. To verify if the installation was successful, test to see if the Husky moves
```
# In one terminal tab
roslaunch husky_gazebo husky_empty_world.launch
# In another terminal tab
rostopic pub /husky_velocity_controller/cmd_vel geometry_msgs/Twist "linear:
        x: 0.5
        y: 0.0
        z: 0.0
angular:
        x: 0.0
        y: 0.0
        z: 0.0" -r 10
```

8. The Husky will be spawned when running the RotorS simulator located in our fork of the [RotorS repository](https://github.com/TRAILab/rotors_simulator)
