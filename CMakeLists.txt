cmake_minimum_required(VERSION 3.0.2)
project(camel-qrbot-ros-jetson)

find_package(catkin REQUIRED COMPONENTS
  roscpp
  sensor_msgs
)

catkin_package()

include_directories(
  include 
  ${catkin_INCLUDE_DIRS}
)

add_library(mcts src/mcts.cpp)
add_library(pcutils src/pcutils.cpp)
