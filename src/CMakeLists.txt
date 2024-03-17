
cmake_minimum_required(VERSION 3.5)
project(pub_sub_test)

## Find catkin and any catkin packages
find_package(catkin REQUIRED COMPONENTS roscpp rospy std_msgs genmsg)
include_directories(${catkin_INCLUDE_DIRS})
link_directories(${catkin_LIBRARY_DIRS})

## Generate added messages and services
generate_messages(DEPENDENCIES std_msgs)

## Declare a catkin package
catkin_package()

## Build publusher and subscriber
include_directories(include ${catkin_INCLUDE_DIRS})

add_executable(pub pub.cpp)
target_link_libraries(pub ${catkin_LIBRARIES})
add_dependencies(pub ${PROJECT_NAME}_generate_messages_cpp)

add_executable(sub sub.cpp)
target_link_libraries(sub ${catkin_LIBRARIES})
add_dependencies(sub ${PROJECT_NAME}_generate_messages_cpp)