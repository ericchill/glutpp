cmake_minimum_required(VERSION 3.5.1)

set(CMAKE_CXX_FLAGS "-O3 -mtune=native")
add_executable(lorenz lorenz2.cpp)
target_link_libraries(lorenz glut GL X11)
