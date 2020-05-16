cmake_minimum_required(VERSION 3.7)
project(cpp_cosole_test)

set(CMAKE_CXX_STANDARD 14)

set(Boost_USE_MULTITHREADED ON)
find_package(Boost COMPONENTS
  system
  filesystem
  REQUIRED)
include_directories(${Boost_INCLUDE_DIRS})

set(SOURCE_FILES main.cpp)
add_executable(${PROJECT_NAME} ${SOURCE_FILES})