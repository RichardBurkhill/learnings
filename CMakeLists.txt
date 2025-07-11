cmake_minimum_required(VERSION 3.15)
project(NewerC++ReleasesDemo)

set(CMAKE_CXX_STANDARD 20)

add_executable(c++20 C++20.cpp)

set(CMAKE_CXX_STANDARD 23)

add_executable(c++23 C++23.cpp)

set(CMAKE_CXX_STANDARD 26)

add_executable(c++26 C++26.cpp)