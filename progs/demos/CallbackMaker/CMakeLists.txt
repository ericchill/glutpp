cmake_minimum_required(VERSION 3.5.1)

add_executable(CallbackMaker CallbackMaker.cpp)
target_link_libraries(CallbackMaker glut GL X11)
