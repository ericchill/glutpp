cmake_minimum_required(VERSION 3.5.1)

add_executable(fractals_random fractals_random.cpp)
target_link_libraries(fractals_random glut GL X11)
