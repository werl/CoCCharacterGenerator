cmake_minimum_required(VERSION 3.17)
project(CoC)

set(CMAKE_CXX_STANDARD 20)

add_executable(CoC src/main.cpp)

add_subdirectory(libs/nana)
add_subdirectory(libs/spdlog)

target_link_libraries(CoC PUBLIC spdlog::spdlog nana::nana)