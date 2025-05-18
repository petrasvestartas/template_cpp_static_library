cmake_minimum_required(VERSION 3.10)
project(template_cpp_static_library VERSION 1.0)

# Specify C++ standard
set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED True)

# Static library
add_library(cpp_static_lib STATIC
    src/calculator.cpp
)

target_include_directories(cpp_static_lib PUBLIC 
    ${CMAKE_CURRENT_SOURCE_DIR}/src
)

# No installation - keep it simple
