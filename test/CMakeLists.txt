# CMakeLists file for unit tests

# Run test writing "make test"

set(TargetName test)

# Add the executable, exclude from build when writing make
add_executable(${TargetName} EXCLUDE_FROM_ALL testmain.cpp)

target_compile_features(${TargetName} PRIVATE cxx_std_20)

target_compile_options(${TargetName} PRIVATE
    -O3
    -Werror
    -Wall
    -Wextra
    -Wpedantic
    )

target_link_libraries(${TargetName} PRIVATE lib)

# Link with the header file catch.hpp for unit tests
target_include_directories(${TargetName} 
    PUBLIC 
    ${PROJECT_SOURCE_DIR}/thirdparty/catch2
    )
