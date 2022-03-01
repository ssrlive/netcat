cmake_minimum_required(VERSION 3.0)

project(netcat)

if(MSVC)
    add_definitions(-D_CRT_SECURE_NO_WARNINGS -D_WINSOCK_DEPRECATED_NO_WARNINGS /wd4996 /wd4133 /wd4244 /wd4312 /wd4267 /wd4311 )
endif(MSVC)

add_executable(nc doexec.c netcat.c getopt.c getopt.h generic.h)
