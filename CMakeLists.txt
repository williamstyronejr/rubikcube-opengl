cmake_minimum_required(VERSION 3.10)
project(openglrubik)

set(CMAKE_CXX_STANDARD 17)

add_executable(main ${PROJECT_SOURCE_DIR}/main.cpp)
SET(EXECUTABLE_OUTPUT_PATH ${PROJECT_BINARY_DIR}/bin)

# OpenGL
find_package(OpenGL REQUIRED)
target_link_libraries(main OpenGL::GL)
include_directories(${OPENGL_INCLUDE_DIRS})

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