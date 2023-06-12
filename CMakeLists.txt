cmake_minimum_required(VERSION 2.8.3)
project(rosbag_to_csv)

find_package(catkin REQUIRED COMPONENTS
  rospy
  rosbag
)

catkin_package(
)

include_directories(
  ${catkin_INCLUDE_DIRS}
)

install(PROGRAMS
  scripts/rosbag_to_csv.py
  scripts/SimplePyQtGUIKit.py
  DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION}
)

install(DIRECTORY
  images
  launch
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
)
