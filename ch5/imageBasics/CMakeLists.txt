cmake_minimum_required( VERSION 2.8 )
project(imageBasics)

set(CMAKE_CXX_FLAGS "-std=c++11")

set(OpenCV_DIR "/Extra/lwy/slam/opencv-3.4.16/build")

find_package( OpenCV REQUIRED)
if (OpenCV_FOUND)
    include_directories(${OpenCV_INCLUDE_DIRS})
    message( ${OpenCV_LIBS})
else()
    message("OpenCV not found, so we won't build the project.")
endif()

add_executable(imageBasics imageBasics.cpp)
# 链接OpenCV库
target_link_libraries(imageBasics ${OpenCV_LIBS})

add_executable(undistortImage undistortImage.cpp)
# 链接OpenCV库
target_link_libraries(undistortImage ${OpenCV_LIBS})
