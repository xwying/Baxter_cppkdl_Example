cmake_minimum_required(VERSION 2.8.3)
project(baxter_cppkdl_example)

find_package(catkin REQUIRED COMPONENTS
  roscpp
  std_msgs
  baxter_cppkdl
)

catkin_package(
  CATKIN_DEPENDS roscpp std_msgs
  DEPENDS
  baxter_cppkdl
)

include_directories(
  ${catkin_INCLUDE_DIRS}
)

add_executable(baxter_kinematics src/baxter_kinematics.cpp)

target_link_libraries(baxter_kinematics ${catkin_LIBRARIES})
