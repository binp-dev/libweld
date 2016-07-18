cmake_minimum_required(VERSION 2.6)
project(libweld)

set(CMAKE_C_FLAGS "${CMAKE_C_FLAGS} -g -Wall")

# add_definitions(-D__XENO__)

set(SOURCE "weld.c")

add_subdirectory(libgl4u)
include_directories(libcandev)

add_library(${PROJECT_NAME} SHARED ${SOURCE})
target_link_libraries(${PROJECT_NAME} candev)
