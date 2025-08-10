cmake_minimum_required(VERSION 3.20)
project(embedded_systems_lab C)

set(CMAKE_C_STANDARD 11)

add_executable(dummy_app
    dummy_main.c
)

target_compile_options(dummy_app PRIVATE -Wall -Wextra -Wpedantic)
