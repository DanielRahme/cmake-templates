# CMake-templates
CMake templates for C/C++ builds.

## Setup
Run these commands in the directory:
```
$ mkdir build
$ cd build
$ cmake ..
$ make
$ ./src/hello
```


## Directory tree
```
.
├── build                   // Output directory
├── CMakeLists.txt          // Top level cmake file
├── inc                     // Header files here
│   └── functions.hpp
├── lib                     // Source files here
│   ├── CMakeLists.txt
│   └── functions.cpp
├── src                     // Executable main files here
│   ├── CMakeLists.txt
│   └── main.cpp
├── test                    // (TODO) Test files here
└── thirdparty              // (TODO) External libraries
```

