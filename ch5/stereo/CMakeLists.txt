cmake_minimum_required( VERSION 2.8 )
project(stereoVision)

set(CMAKE_CXX_FLAGS "-std=c++11")

set(OpenCV_DIR "/Extra/lwy/slam/opencv-3.4.16/build")


# Opencv
find_package(OpenCV REQUIRED)
include_directories(${OpenCV_INCLUDE_DIRS})

# Eigen
include_directories("/usr/include/eigen3")

## Pangolin
find_package(Pangolin REQUIRED)

add_executable(stereoVision stereoVision.cpp)
#lib
target_link_libraries(stereoVision ${OpenCV_LIBS} ${Pangolin_LIBRARIES})