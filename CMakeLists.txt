cmake_minimum_required(VERSION 2.8.3)
project(robotiq_ros_pkg)

## Uncomment if the package has a setup.py
catkin_python_setup()

find_package(catkin REQUIRED COMPONENTS roslaunch rospy message_generation std_msgs)

add_message_files(FILES
  GripperCmd.msg
  GripperStat.msg
)

generate_messages(DEPENDENCIES
  std_msgs
)
