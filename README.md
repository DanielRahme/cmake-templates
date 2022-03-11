# CMake-templates
CMake templates for C/C++ builds.
With unit test using doctest framework.

## Setup
Run these commands in the directory:
```
$ mkdir build
$ cd build
$ cmake ..
$ make
$ ./src/hello
```

## Test
Run all tests using CTest by entering the following command in build directory:

    $ make test

The tests will be compiled in the `/build/test/` folder and using [doctest](https://github.com/doctest/doctest) for unit tests:

    $ ./test/my_test

## Directory structure
```
.
├── build
├── cmake
│   └── Finddoctest.cmake
├── CMakeLists.txt
├── include
│   └── functions.hpp
├── lib
│   ├── CMakeLists.txt
│   └── functions.cpp
├── LICENSE
├── README.md
├── src
│   ├── CMakeLists.txt
│   └── main.cpp
└── test
    ├── CMakeLists.txt
    └── testmain.cpp
```

