cmake_minimum_required (VERSION 2.8)
project (quectel-CM)

set (SRCS GobiNetCM.c main.c MPQMUX.c QMIThread.c QmiWwanCM.c util.c)

add_definitions(-g -O2 -pipe -Wall -Wextra)
add_definitions(-DNDEBUG)

add_executable (quectel-CM ${SRCS})

target_link_libraries (quectel-CM pthread rt)

install (TARGETS quectel-CM RUNTIME DESTINATION sbin)
