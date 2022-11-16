cmake_minimum_required(VERSION 3.14)

set(CMAKE_CXX_STANDART 17)

project(profiler_linux)

find_package(Curses REQUIRED)

include_directories(${CURSES_INCLUDE_DIR})

add_executable(Profiler Profiler.cpp
                        ../engine/Engine.h ../engine/Engine.cpp
                        ../engine/TypesAndConsts.h
                        ../invalidbot/InvalidBot.h)

target_link_libraries(Profiler ${CURSES_LIBRARIES})

