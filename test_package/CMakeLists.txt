cmake_minimum_required(VERSION 3.15)
cmake_policy(SET CMP0074 NEW)

project(test_package CXX)
set(CMAKE_VERBOSE_MAKEFILE TRUE)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

find_package(ebml REQUIRED CONFIG)
find_package(matroska REQUIRED CONFIG)
add_executable(${PROJECT_NAME} test_package.cpp)
target_link_libraries(${PROJECT_NAME} matroska::matroska EBML::ebml)
