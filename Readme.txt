This project uses ROS2 humble and gazebo harmonic.

It uses turtlebot3_gazebo package from source and nav2_bringup from binary.

To intialize the simulation and all the plugins.

	ros2 launch nav_planner naviagtor.launch.py 

To navigate the amr in the environment.

        ros2 run nav_planner navigator_final.py
        
To cancel the tasks:
        
        
        ros2 topic pub --once /cancel_task std_msgs/msg/Bool "data: true"

To cancel the order:

	ros2 topic pub --once /cancel_order std_msgs/String "data: 'table2'"
