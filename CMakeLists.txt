cmake_minimum_required(VERSION 3.15)
project(openglrubik)

set(CMAKE_CXX_STANDARD 17)

add_executable(main main.cpp)

# OpenGL
find_package(OpenGL REQUIRED)
target_link_libraries(main OpenGL::GL)

# GLFW
set(GLFW_BUILD_DOCS OFF CACHE BOOL "" FORCE)
set(GLFW_BUILD_TESTS OFF CACHE BOOL "" FORCE)
set(GLFW_BUILD_EXAMPLES OFF CACHE BOOL "" FORCE)

add_subdirectory(vendor/glfw)
include_directories(vendor/glfw/include)
target_link_libraries(main glfw)

if (APPLE)
  target_link_libraries(main "-framework OpenGL")
endif()                                             