project(Library)

set(LibName Libs)
add_library(${LibName}
    functions.cpp
    )

# Link with the header files in inc
target_include_directories(${LibName} PUBLIC 
    "${CMAKE_CURRENT_SOURCE_DIR}/../../inc"
    )

# Set the language standard to C++17 for target
target_compile_features(${LibName} PRIVATE cxx_std_17)

# Keep the generated assembly files
set_target_properties(${LibName} PROPERTIES COMPILE_FLAGS -save-temps)

# Compiler flags for target
target_compile_options(${LibName} PRIVATE
    -O3
    -Werror
    -Wall
    -Wextra
    -Wpedantic
    )
