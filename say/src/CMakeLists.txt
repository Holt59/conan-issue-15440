cmake_minimum_required(VERSION 3.15)

add_library(say say.cpp)
target_include_directories(say PUBLIC $<BUILD_INTERFACE:${CMAKE_SOURCE_DIR}/include>)
target_include_directories(say
    SYSTEM PUBLIC
    $<INSTALL_INTERFACE:$<INSTALL_PREFIX>/include>)
install(TARGETS say)
