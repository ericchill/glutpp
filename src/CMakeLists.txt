cmake_minimum_required(VERSION 3.20.0)
include(GenerateExportHeader)

set(CMAKE_BUILD_TYPE Debug)
set(BUILD_SHARED_LIBS)

file(GLOB SOURCES "*.cpp")

set(LIB_SOURCES ${SOURCES})
list(REMOVE_ITEM LIB_SOURCES tester.cpp)

add_definitions(-std=c++20)
add_library(glutpp SHARED ${LIB_SOURCES})
add_library(glutpptest STATIC ${LIB_SOURCES})
GENERATE_EXPORT_HEADER(glutpp
             BASE_NAME glutpp
             EXPORT_MACRO_NAME glutpp_EXPORT
             EXPORT_FILE_NAME glutpp_Export.h
             STATIC_DEFINE glutpp_BUILT_AS_STATIC
)

target_link_libraries(glutpp GL X11 Xext xmu pthread)

set_target_properties(glutpp PROPERTIES
  VERSION 0.0.1
  SOVERSION 0
  )

add_executable(tester tester.cpp ${LIB_SOURCES})
target_link_libraries(tester GL X11 Xext Xmu pthread)

install(TARGETS glutpp DESTINATION lib)
