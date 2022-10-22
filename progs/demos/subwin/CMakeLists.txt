cmake_minimum_required(VERSION 3.5.1)

add_executable(subwin subwin.cpp)
target_link_libraries(subwin glut GL X11)
