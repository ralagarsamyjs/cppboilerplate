cmake_minimum_required(VERSION 3.10)
project(cpp_workspace)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

include_directories(include)

add_executable(app
    src/main.cpp
    src/stringTest.cpp
)