cmake_minimum_required(VERSION 3.18.0)
project(project3 VERSION 1.0.0)
cmake_policy(SET CMP0072 NEW)

set(CMAKE_CXX_STANDARD 20)

find_package(OpenGL REQUIRED)

add_executable(project3
    src/config.h
    src/config.cpp
    src/main.cpp 
    src/glad.c
    src/processInput.cpp
    src/cube.cpp
    src/camera.cpp
    )

# Specify the include directory for GLFW headers
target_include_directories(project3 PRIVATE "${CMAKE_CURRENT_SOURCE_DIR}/include/")

# Link against GLFW library
target_link_libraries(project3 "C:/Users/morte/OneDrive - Danmarks Tekniske Universitet/Project3/include/lib/libglfw3dll.a" OpenGL::GL)