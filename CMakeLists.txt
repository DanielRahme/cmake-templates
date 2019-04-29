cmake_minimum_required(VERSION 3.13.0)

# The project name
project(Hello)

# Name of the executable
set(TARGET_NAME hello)

# Include the header files
include_directories(${CMAKE_CURRENT_SOURCE_DIR}/inc)

# Include the source files
file(GLOB SOURCES "src/*.cpp")

# The executable 
add_executable(${TARGET_NAME} ${SOURCES})

# The language standard, C++17
set_property(TARGET ${TARGET_NAME} PROPERTY CXX_STANDARD 17)

# Compiler flags
target_compile_options(${TARGET_NAME} PRIVATE
    -Werror
    -Wall
    -Wextra
    -Wpedantic)
