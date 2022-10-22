cmake_minimum_required(VERSION 3.5.1)

add_executable(one one.cpp)
target_link_libraries(one glut GL X11)
