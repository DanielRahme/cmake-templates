
project(UnitTest)

# Run test writing "make test"
set(TargetName test)
# Add the executable, exclude from running when writing make
add_executable(${TargetName} EXCLUDE_FROM_ALL testmain.cpp)

# Use C++17 standard
set_target_properties(${TargetName} PROPERTIES  CXX_STANDARD 17)

# Compiler flags for target
target_compile_options(${TargetName} PRIVATE
    -O3
    -Werror
    -Wall
    -Wextra
    -Wpedantic
    )

# Link with included libraries from /lib
target_link_libraries(${TargetName} PRIVATE Libs)

# Link with the header file catch.hpp for unit tests
target_include_directories(${TargetName} PUBLIC 
    "${CMAKE_CURRENT_SOURCE_DIR}/../thirdparty/catch2"
    )
