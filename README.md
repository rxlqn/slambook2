## 12_26
- exp 中是自己做的实验
- 其他是参考
- 先cmake . 生成编译文件 makefile
- 再make -j8 调用g++
- 生成可执行文件后可以用gdb调试

- mkdir build && cd build
- set(CMAKE_CXX_FLAGS "-std=c++11")
- export DISPLAY=:10

## 12_27
- c_cpp_properties.json is used with Intellisense and in no way deals with compilation.
- gdb调试不需要预先build，所以不需要preLaunchTask
- Release   就不能调试了
    - set(CMAKE_BUILD_TYPE "Release")
    - set(CMAKE_CXX_FLAGS "-O3")
- 调试模式
    - set(CMAKE_BUILD_TYPE "Debug")

- opencv
    export PKG_CONFIG_PATH=/Extra/lwy/slam/opencv/lib/pkgconfig
    export LD_LIBRARY_PATH=/Extra/lwy/slam/opencv/lib

    sudo apt-get install build-essential libgtk2.0-dev libvtk5-dev libjpeg-dev libtiff4-dev libjasper-dev libopenexr-dev libtbb-dev

## 12_29
- ceres
    sudo apt-get install liblapack-dev libsuitesparse-dev libcxsparse3.1.4 libgflags-dev libgoogle-glog-dev libgtest-dev

## 12_30
- set(OpenCV_DIR "/Extra/lwy/slam/opencv-3.4.16/build")
    - export OpenCV_DIR=:"/Extra/lwy/slam/opencv-3.4.16/build"

## 1_13
- g2o
    sudo apt-get install qt5-qmake qt5-default libqglviewer-dev-qt5 libsuitesparse-dev libcxsparse3 libcholmod3