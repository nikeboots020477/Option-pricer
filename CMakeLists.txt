cmake_minimum_required(VERSION 3.12)
project(OptionEstimator)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_EXPORT_COMPILE_COMMANDS ON)

find_package(PostgreSQL REQUIRED)
include_directories(${CMAKE_SOURCE_DIR}/include)

add_executable(main main.cpp src/control.cpp)
#target_link_libraries(main control)
target_link_libraries(main PRIVATE PostgreSQL::PostgreSQL)
