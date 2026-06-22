
gz service -s /gui/follow/offset   --reqtype gz.msgs.Vector3d   --reptype gz.msgs.Boolean   --timeout 1000   --req 'x: -1.5, y: 0.0, z: 1.0'

 ros2 launch nav2_bringup localization_launch.py use_sim_time:=True autostart:=True map:=/home/rishi/nav_ws/src/nav_planner/maps/my_map.yaml

 ros2 launch nav2_bringup navigation_launch.py use_sim_time:=True autostart:=True map:=/home/rishi/nav_ws/src/nav_planner/maps/my_map.yaml

 ros2 launch turtlebot3_gazebo turtlebot3_world.launch.py 


ros2 topic pub --once /cancel_order std_msgs/String "data: 'table2'"

ros2 topic pub --once /cancel_task std_msgs/msg/Bool "data: true"
