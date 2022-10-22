cmake_minimum_required(VERSION 3.5.1)

add_executable(smooth_opengl3 smooth_opengl3.cpp)
target_link_libraries(smooth_opengl3 glut GL X11)
