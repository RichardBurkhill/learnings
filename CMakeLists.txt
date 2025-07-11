cmake_minimum_required(VERSION 3.14)
project(Cpp14DemoTests)

# Enable testing framework
enable_testing()

# Use C++14
set(CMAKE_CXX_STANDARD 14)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

# Set GTest paths (change if you’re not using /opt/homebrew)
set(GTEST_ROOT /opt/homebrew/opt/googletest)

# Add include directories for GTest/GMock
include_directories(${GTEST_ROOT}/include)
link_directories(${GTEST_ROOT}/lib)

# Add your test source file
add_executable(Cpp14DemoTests ../CPlusPlus/main.cpp)

# Link against GTest, GMock, and pthread
target_link_libraries(Cpp14DemoTests
    gtest
    gmock
    gtest_main
    pthread
)

# Enable CTest if desired
add_test(NAME Cpp14DemoTests COMMAND Cpp14DemoTests)

# Use C++14
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

# Add your test source file
add_executable(c++17  C++17.cpp)