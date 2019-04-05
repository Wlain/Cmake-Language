cmake_minimum_required(VERSION 3.2)
project(SampleLibrary)

add_library(hellolib STATIC
  hellolib.cpp
  hellolib.h
)

add_executable(helloworld helloworld.cpp)

target_link_libraries(helloworld hellolib)
