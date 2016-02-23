cmake_minimum_required(VERSION 2.8.3)
project(semap_msgs)

find_package(catkin REQUIRED COMPONENTS
  roscpp
  mesh_msgs
  geometry_msgs
  visualization_msgs
  message_generation
)

add_message_files( DIRECTORY msg )

generate_messages(
  DEPENDENCIES
  mesh_msgs
  geometry_msgs
  visualization_msgs
)

catkin_package(
  INCLUDE_DIRS
  CATKIN_DEPENDS
    roscpp
    mesh_msgs
    geometry_msgs
    visualization_msgs
)
