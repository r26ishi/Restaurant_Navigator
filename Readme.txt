# ROS2 Navigation Project

This project uses **ROS 2 Humble**, **Gazebo Harmonic**, the **`turtlebot3_gazebo`** package built from source, and **`nav2_bringup`** installed from binary packages.

## Prerequisites

- ROS 2 Humble
- Gazebo Harmonic
- `turtlebot3_gazebo` package built from source
- `nav2_bringup` installed from binary packages

---

## Launch the Simulation

To initialize the simulation environment and load all required plugins, run:

```bash
ros2 launch nav_planner naviagtor.launch.py
```

---

## Start Navigation

To navigate the AMR within the environment, run:

```bash
ros2 run nav_planner navigator_final.py
```

---

## Cancel the Current Navigation Task

To cancel the active navigation task:

```bash
ros2 topic pub --once /cancel_task std_msgs/msg/Bool "data: true"
```

---

## Cancel an Order

To cancel a specific order (for example, `table2`):

```bash
ros2 topic pub --once /cancel_order std_msgs/msg/String "data: 'table2'"
```

---

## Project Stack

| Component | Description |
|------------|-------------|
| ROS Version | ROS 2 Humble |
| Simulator | Gazebo Harmonic |
| Robot Package | `turtlebot3_gazebo` (source build) |
| Navigation | `nav2_bringup` (binary installation) |
| Navigation Node | `navigator_final.py` |

---
