cmake_minimum_required(VERSION 2.8)

project(linux_lab_rab)
set(CMAKE_C_FLAGS "-std=c99")

add_executable(komppl komppl.c)

add_executable(komassr kompassr.c)

find_package(Curses REQUIRED)
include_directories(${CURSES_INCLUDE_DIR})
add_executable(absload absloadm.c)
target_link_libraries(absload ${CURSES_LIBRARIES})

