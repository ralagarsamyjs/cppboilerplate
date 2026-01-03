# cppboilerplate

# C++ Base Project

This repository contains a basic C++ repository using CMake + VS Code. End-to-end guide to build a basic C++ repository

## Prerequisites

- CMake
- Clang or GCC
- VS Code (optional)

## Build Steps

1. CMake-based C++ project
2. Configure CMake
3. Launch (Run / Debug)

### STEP 1 — Create a CMake-based C++ project (the base repo)

cpp-base/
├── CMakeLists.txt
├── src/
│ └── main.cpp
├── include/
├── .vscode/
│ ├── tasks.json
│ ├── launch.json
│ └── c_cpp_properties.json
└── build/ # generated (never commit)

## CMakeLists.txt (root)

```bash
cmake_minimum_required(VERSION 3.10)
project(cpp_base LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_executable(app
src/main.cpp
)
```

### STEP 2 — Configure CMake (this is the MOST IMPORTANT step)

What “Configure” really means

CMake reads CMakeLists.txt
Generates build system files into build/
Creates CMakeCache.txt
Discovers compiler + flags

Configure via terminal (always works)

```bash
cmake -S . -B build
```

Configure via VS Code (optional)

```bash
Cmd + Shift + P → CMake: Configure
```

### STEP 3 — Launch (Run / Debug)

What “Launch” means

Run the already built executable
Attach debugger
Handle breakpoints

How launch actually works

When you press F5:

VS Code runs preLaunchTask → build
build/app must exist
LLDB attaches
Program starts
Breakpoints work
