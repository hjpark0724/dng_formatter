cmake_minimum_required(VERSION 3.29)
project(dng_formatter C)

set(CMAKE_C_STANDARD 11)
# file(GLOB SOURCES "${CMAKE_SOURCE_DIR}/libtiff/libtiff/*.c")
set(SOURCES
        libtiff/libtiff/tif_warning.c
        libtiff/libtiff/tif_error.c
        libtiff/libtiff/tif_unix.c

)

include_directories(${CMAKE_SOURCE_DIR}/libtiff)
message("source: ${SOURCES}")
add_executable(dng_formatter main.c ${SOURCES})
target_link_libraries(dng_formatter m)