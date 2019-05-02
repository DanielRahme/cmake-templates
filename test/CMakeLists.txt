
project(UnitTest)

# Add the executable target
set(TargetName testmain)
add_executable(${TargetName} testmain.cpp)

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
