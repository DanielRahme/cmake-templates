# CMake-templates
CMake templates for C/C++ builds.
With unit test using Catch2 framework.

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
├── build               # Output files
├── CMakeLists.txt      # Top-level cmake file
├── inc                 # All public headers go here
├── src                 # Source files
│   ├── CMakeLists.txt
│   ├── lib             # Library source files
│   └── main.cpp
├── test                # Unit tests
│   ├── CMakeLists.txt
│   └── testmain.cpp
└── thirdparty          # 3rd-party libraries
```

