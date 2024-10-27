cmake_minimum_required(VERSION 3.10)
project("sdl-template" VERSION 0.1 LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_EXPORT_COMPILE_COMMANDS ON)

include_directories(include)
include_directories(libs/sdl/include)

file(GLOB SOURCES "src/*.cpp")

add_executable(${PROJECT_NAME} main.cpp ${SOURCES})

add_subdirectory(libs/sdl)

target_link_libraries(${PROJECT_NAME} PRIVATE SDL3::SDL3)
