cmake_minimum_required(VERSION 3.10)
project(Lab2)

include_directories(include)

add_library(mylib STATIC src/mylib.c)

add_executable(lab2 src/main.c)

target_link_libraries(lab2 mylib)
