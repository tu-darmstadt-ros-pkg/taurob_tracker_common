cmake_minimum_required(VERSION 2.8.3)
project(taurob_tracker_description)

## Find catkin macros and libraries
## if COMPONENTS list like find_package(catkin REQUIRED COMPONENTS xyz)
## is used, also find other catkin packages
find_package(catkin REQUIRED COMPONENTS
  hector_components_description
  hector_xacro_tools
  urdf
  xacro
)

catkin_package(
#  INCLUDE_DIRS include
#  LIBRARIES taurob_tracker_description
#  CATKIN_DEPENDS hector_components_description hector_xacro_tools urdf xacro
#  DEPENDS system_lib
)

include_directories(
  ${catkin_INCLUDE_DIRS}
)

install(DIRECTORY urdf meshes launch rviz
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
)