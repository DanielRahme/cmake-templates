# Top-level CMake file
cmake_minimum_required(VERSION 3.13.0)

# The project name, version and languages
project(Hello VERSION 1.0 LANGUAGES CXX)

# Add the CMakeFiles in the other directories
add_subdirectory(src)
add_subdirectory(lib)
