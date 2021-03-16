cmake_minimum_required(VERSION 3.16)
project(TermTyper)
set(CMAKE_CXX_STANDARD 20)

find_package(Curses REQUIRED)
include_directories(${CURSES_INCLUDE_DIR})

add_subdirectory(libraries)
include_directories(${PROJECT_SOURCE_DIR}/libraries)
add_executable(TermTyper main.cpp)

target_link_libraries(TermTyper ${CURSES_LIBRARIES} libTermTyper)