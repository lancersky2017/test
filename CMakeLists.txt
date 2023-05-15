cmake_minimum_required(VERSION 3.0)

project(test C)

add_definitions(-D_GNU_SOURCE)
add_compile_options(-g -O -Wall -Werror --std=gnu99)

set(EXEC_NAME "test")

aux_source_directory(. SOURCES)
add_executable(${EXEC_NAME} ${SOURCES})

INSTALL(TARGETS ${EXEC_NAME} RUNTIME DESTINATION bin)

