# Rubik Cube 
A cross-platform app of a playable rubik cube using C++ and OpenGL.

## Build Steps

### Install dependencies

#### Windows
##### CMake
Download and install [CMake](http://www.cmake.org/cmake/resources/software.html).


#### Linux 
##### CMake, xOrg, Mesa
    sudo apt-get install cmake xorg-dev libgl1-mesa-dev
    
#### MacOS
##### CMake
Download and install [CMake](http://www.cmake.org/cmake/resources/software.html).

### Compile and Run
    git clone https://github.com/williamstyronejr/rubikcube-opengl.git -recursive
    cd rubikcube-opengl
    cmake .
    make .
    ./bin/main