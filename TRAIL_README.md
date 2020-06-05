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

6. Build the package
```
catkin build
```

7. The Husky will be spawned when running the RotorS simulator located in our fork of the [RotorS repository](https://github.com/TRAILab/rotors_simulator)
