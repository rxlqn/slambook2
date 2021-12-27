# 12_26
- exp 中是自己做的实验
- 其他是参考
- 先cmake . 生成编译文件 makefile
- 再make 调用g++
- 生成可执行文件后可以用gdb调试

- mkdir build && cd build
- set(CMAKE_CXX_FLAGS "-std=c++11")
- export DISPLAY=:11

## 12_27
- c_cpp_properties.json is used with Intellisense and in no way deals with compilation.
- gdb调试不需要预先build，所以不需要preLaunchTask
- Release   就不能调试了
    - set(CMAKE_BUILD_TYPE "Release")
    - set(CMAKE_CXX_FLAGS "-O3")
- 调试模式
    - set(CMAKE_BUILD_TYPE "Debug")


