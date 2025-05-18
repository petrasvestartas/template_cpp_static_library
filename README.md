# C++ Static Library Template

A template project for creating a C++ static library using CMake. The library includes a simple function to sum two integers as a demonstration.

## Project Structure

```
template_cpp_static_library/
├── CMakeLists.txt       # CMake configuration file
├── README.md           # This file
└── src/                # Source directory
    ├── calculator.cpp  # Implementation file
    └── calculator.h    # Header file
```

## Prerequisites

- CMake (version 3.10 or higher)
- C++ compiler supporting C++11

## Building the Library

Follow these steps to build the static library:

1. Create a build directory:
   ```bash
   mkdir -p build
   cd build
   ```

2. Generate the build system:
   ```bash
   cmake ..
   ```

3. Build the library:
   ```bash
   make
   ```

After successful compilation, the static library file `libcpp_static_lib.a` will be created in the build directory.

## Using the Library

To use this library in another project, you can:

1. Include the header file directly from the src directory:
   ```cpp
   #include "path/to/template_cpp_static_library/src/calculator.h"
   
   int result = math::sum(5, 7); // Returns 12
   ```

2. Link with the library in your CMake project:
   ```cmake
   # In your CMakeLists.txt
   add_subdirectory(path/to/template_cpp_static_library)
   target_link_libraries(your_target PRIVATE cpp_static_lib)
   ```