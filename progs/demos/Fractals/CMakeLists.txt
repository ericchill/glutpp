cmake_minimum_required(VERSION 3.5.1)

add_executable(fractals fractals.cpp)
target_link_libraries(fractals glut GL X11)
