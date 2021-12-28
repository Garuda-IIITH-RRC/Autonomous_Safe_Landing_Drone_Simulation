# Autonomous-Safe-Landing-UAV

main instructions is to source respective mavros folder- map is changed to local_origin 

set  COM_OBS_AVOID = 1 in QGC parameters

check rviz folder without flying -  for green zone

change 2 params in rqt to set the tuning for safe landing

check mavros_posix_sitl.launch for downfacing camera 

## How To Run Simulation

1. Terminal 1st:-
```bash
cd PX4-Autopilot
source ~/(wherever simulation workspace is installed)/devel/setup.bash
source Tools/setup_gazebo.bash $(pwd) $(pwd)/build/px4_sitl_default
export ROS_PACKAGE_PATH=$ROS_PACKAGE_PATH:$(pwd)
export ROS_PACKAGE_PATH=$ROS_PACKAGE_PATH:$(pwd)/Tools/sitl_gazebo
roslaunch px4 mavros_posix_sitl.launch
```
2. Terminal 2nd:-
```bash
cd catkin_ws/
source devel/setup.bash
roslaunch safe_landing_planner safe_landing_planner.launch
```
3. Terminal 2nd:-
```bash
cd catkin_ws/
source devel/setup.bash
roslaunch safe_landing_planner rviz.launch
```
