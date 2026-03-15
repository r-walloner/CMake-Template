cmake_minimum_required(VERSION 3.10)
project(Main)
set(CMAKE_CXX_STANDARD 23)

add_executable(${CMAKE_PROJECT_NAME} src/main.cpp)

if (MSVC)
    target_compile_options(${CMAKE_PROJECT_NAME} PRIVATE /permissive- /W4)
else ()
    target_compile_options(${CMAKE_PROJECT_NAME} PRIVATE -Wall -Weffc++ -Wextra -Wpedantic -Wconversion -Wsign-conversion -Wshadow)
endif ()
