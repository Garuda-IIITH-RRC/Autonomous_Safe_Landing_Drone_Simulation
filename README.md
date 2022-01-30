# Autonomous-Safe-Landing-Drone



## How To Run Simulation

### Terminal 1:-
```bash
cd PX4-Autopilot
source ~/(wherever simulation workspace is installed)/devel/setup.bash
source Tools/setup_gazebo.bash $(pwd) $(pwd)/build/px4_sitl_default
export ROS_PACKAGE_PATH=$ROS_PACKAGE_PATH:$(pwd)
export ROS_PACKAGE_PATH=$ROS_PACKAGE_PATH:$(pwd)/Tools/sitl_gazebo
roslaunch px4 mavros_posix_sitl.launch
```
### Terminal 2:-
```bash
cd catkin_ws/
source devel/setup.bash
roslaunch safe_landing_planner safe_landing_planner.launch
```
### Note:-
safe_landing_planner.launch launches the required nodes(safe_landing_planner and waypoint_generator) along with Rviz\
main instructions is to source respective mavros folder- map is changed to local_origin \
check mavros_posix_sitl.launch for downfacing camera\
set  COM_OBS_AVOID = 1 in QGC parameters\
check rviz folder without flying -  for green zone\
change 2 params in rqt to set the tuning for safe landing\

### Simulation Demo:-
<img src="https://github.com/Garuda-IIITH-RRC/Autonomous_Safe_Landing_Drone_Simulation/blob/master/land_simulation.gif" width="1000" height="300">

### Youtube links:-

[![](https://img.youtube.com/vi/377WQKVdjBY/0.jpg)](https://www.youtube.com/watch?v=377WQKVdjBY)\
[![](https://img.youtube.com/vi/IrvUYQut9FI/0.jpg)](https://www.youtube.com/watch?v=IrvUYQut9FI)
