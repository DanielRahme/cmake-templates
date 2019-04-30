project(Executables)

# Add the executable target
set(TargetName hello)
add_executable(${TargetName} main.cpp)

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
