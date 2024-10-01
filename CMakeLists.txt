cmake_minimum_required(VERSION 3.29)
project(MCML C)

set(CMAKE_C_STANDARD 90)

add_executable(MCML
        mcml.h
        mcmlio.c
        mcmlnr.c
        mcmlgo.c
        mcmlmain.c)
