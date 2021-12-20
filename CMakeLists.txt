#
# CMakeLists.txt
# Copyright (C) 2021 Marius Greuel
#

cmake_minimum_required(VERSION 3.12)
project(libhidapi)

add_library(libhidapi STATIC
    src/hid.c
    )

target_include_directories(libhidapi
    PUBLIC
    include
    PRIVATE
    include/hidapi
    )

if(MSVC)
    target_compile_options(libhidapi PRIVATE /wd4267) # warning C4267: 'function': conversion from 'xxx' to 'xxx', possible loss of data
    target_compile_options(libhidapi PRIVATE /wd5105) # warning C5105: macro expansion producing 'xxx' has undefined behavior
endif()
