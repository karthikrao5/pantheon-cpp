cmake_minimum_required(VERSION 3.12)
project(pantheon_cpp)

set(CMAKE_CXX_STANDARD 14)

include_directories(include)

add_subdirectory(libs/glfw-3.3.2)
include_directories(libs/glfw-3.3.2/include)

add_executable(pantheon_cpp main.cpp glad.c include/linmath.h)

target_link_libraries(pantheon_cpp glfw ${GLFW_LIBRARIES})