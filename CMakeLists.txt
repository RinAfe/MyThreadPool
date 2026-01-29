cmake_minimum_required(VERSION 4.1)
project(MyThreadPool)

set(CMAKE_CXX_STANDARD 17)

include_directories(MyThreadPool/include)

add_executable(MyThreadPool
        MyThreadPool/include/MyThreadPool.h
        MyThreadPool/src/MyThreadPool.cpp
        MyThreadPool/main.cpp)
