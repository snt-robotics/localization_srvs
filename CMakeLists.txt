cmake_minimum_required(VERSION 2.8.3)
project(localization_srvs)


find_package(catkin REQUIRED COMPONENTS
  geometry_msgs
  message_generation
)

add_service_files(
  DIRECTORY srv
  FILES
  ConfigureInitialYawRobotInWorld.srv
  ConfigureInitialPositionRobotInWorld.srv
  ConfigureInitialPoseRobotInWorld.srv
)

generate_messages(
  DEPENDENCIES
  geometry_msgs
)

catkin_package(
  CATKIN_DEPENDS message_runtime geometry_msgs
)

#include_directories(${catkin_INCLUDE_DIRS})
