# Minimum CMake VERSION
cmake_minimum_required(VERSION 3.0)

# Project Name
project(CMakePractice)

# Version Number Set (Variables)
set(CMakePractice_VERSION_MAJOR 1)
set(CMakePractice_VERSION_MINOR 0)

# Directory Includes
include_directories(libraries)
include_directories(libraries/header)
include_directories(libraries/header/in)
include_directories(sources)

# Header File Configure
configure_file(
    "libraries/header/in/CMakePracticeConfig.h.in"
    "libraries/header/CMakePracticeConfig.h"
	)

# build -> exe
add_executable(CMakePractice sources/main.cpp)