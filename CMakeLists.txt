cmake_minimum_required(VERSION 3.10)
project(MRC_Spec_Repository C)

set(CMAKE_C_STANDARD 99)

include_directories(include)

add_library(mrc_stub STATIC
    src/mrc_stub.c
)
