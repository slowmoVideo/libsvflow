# Follows this post: https://stackoverflow.com/a/45843676/271961

cmake_minimum_required(VERSION 3.0)

project(libsvflow VERSION 1.0.0 DESCRIPTION "Library for optical flow files")

set(LIB_SRC_FLOW
        src/flowRW_sV.cpp
        src/flowField_sV.cpp
        )
set(HEADERS
        include/flowRW_sV.h
        include/flowField_sV.h
        )


add_library(sVflow STATIC ${LIB_SRC_FLOW})
set_target_properties(sVflow PROPERTIES VERSION ${PROJECT_VERSION})
target_include_directories(sVflow PUBLIC src)
target_include_directories(sVflow PUBLIC include)
