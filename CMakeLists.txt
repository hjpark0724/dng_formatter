cmake_minimum_required(VERSION 3.29)
project(dng_formatter C)

set(CMAKE_C_STANDARD 11)
# file(GLOB SOURCES "${CMAKE_SOURCE_DIR}/libtiff/libtiff/*.c")
set(SOURCES
        libtiff/libtiff/tif_warning.c
        libtiff/libtiff/tif_error.c
        libtiff/libtiff/tif_aux.c
        libtiff/libtiff/tif_hash_set.c
        libtiff/libtiff/tif_dir.c
        libtiff/libtiff/tif_dirinfo.c
        libtiff/libtiff/tif_dirread.c
        libtiff/libtiff/tif_dirwrite.c
        libtiff/libtiff/tif_tile.c
        libtiff/libtiff/tif_swab.c
        libtiff/libtiff/tif_codec.c
        libtiff/libtiff/tif_compress.c
        libtiff/libtiff/tif_dumpmode.c
        libtiff/libtiff/tif_strip.c
        libtiff/libtiff/tif_unix.c
        libtiff/libtiff/tif_open.c
        libtiff/libtiff/tif_close.c
        libtiff/libtiff/tif_read.c
        libtiff/libtiff/tif_write.c
        libtiff/libtiff/tif_flush.c
)

include_directories(${CMAKE_SOURCE_DIR}/libtiff)
message("source: ${SOURCES}")
add_executable(dng_formatter main.c ${SOURCES})
target_link_libraries(dng_formatter m)