cmake_minimum_required(VERSION 3.5.1)

add_executable(shapes shapes.cpp)
target_link_libraries(shapes glut GL X11)
