cmake_minimum_required(VERSION 3.25)

# Print build type
message(STATUS "Build type: ${CMAKE_BUILD_TYPE}")

###########################################################
# Use C++20
set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED true)
set(CMAKE_CXX_EXTENSIONS false)

###########################################################
# Testing. Should not be enabled!
add_compile_options("-Weverything")
add_compile_options("-Wall")
add_compile_options("-Wextra")
add_compile_options("-Werror")

###########################################################
# Our project
project("build-counter"
	VERSION 0.1.0
	DESCRIPTION "A small tool to count build numbers and create build timestamps."
	LANGUAGES CXX
)

# Main executable
add_executable("${PROJECT_NAME}"
	src/Main.cpp
)
