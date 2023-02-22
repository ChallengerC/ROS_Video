cmake_minimum_required(VERSION 3.0.2)
project(videototopic)
SET(OpenCV_DIR /usr/local/share/OpenCV)

find_package(catkin REQUIRED COMPONENTS
  cv_bridge
  image_transport
  roscpp
  OpenCV
)


catkin_package(

)

include_directories(
  ${catkin_INCLUDE_DIRS}
  ${OpenCV_INCLUDE_DIRS}
)

add_executable(videototopic src/videototopic.cpp)

target_link_libraries(${PROJECT_NAME}
  ${catkin_LIBRARIES}
  ${OpenCV_LIBS}
)

