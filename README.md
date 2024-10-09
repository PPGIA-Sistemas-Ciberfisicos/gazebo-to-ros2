# gazebo to ros2

This package aims to create a simple scene in Gazebo with a LiDAR inside a warehouse. Additionally, it initializes the `gzbridge` that connects the Gazebo and ROS 2 topics.

## Prerequisites

- **ROS 2** (Foxy, Galactic, Humble, or later)
- **Gazebo** compatible with the installed ROS 2 version

## Cloning the Repository
Clone the repository inside the source folder of your ROS 2 workspace (**ros2_ws/src**):

```bash
cd ros2_ws/src/
git clone https://github.com/PPGIA-Sistemas-Ciberfisicos/gazebo-to-ros2.git
```

## Building the Package

After cloning the repository, navigate to the package directory and build it using colcon:

```bash
cd ros2_ws/
colcon build
```

Don't forget to source the environment after building:

```bash
source install/setup.bash
```

## Running the simulation

To start the scene in Gazebo and initialize the `gzbridge`, run:

```bash
ros2 launch gazebo_gz_to_ros2_simples husky_LiDAR_Dept.launch.py
```

To start only the gazebo simulation run:

```bash
ros2 launch ros_gz_sim gz_sim.launch.py gz_args:="~/ros2_ws/src/gazebo_gz_to_ros2_simples/gz_sim/worlds/husky/husky_LiDAR_Dept.sdf"
```
> [!WARNING]
> Remember to change **ros2_ws/** to your ros2 workspace folder