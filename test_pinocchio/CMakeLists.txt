cmake_minimum_required(VERSION 3.4)

project(myproject)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED True)
SET(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -pthread")

find_package(pinocchio REQUIRED)

add_executable(check_pinocchio_version src/check_pinocchio_version.cpp)

target_link_libraries(check_pinocchio_version pinocchio::pinocchio)
