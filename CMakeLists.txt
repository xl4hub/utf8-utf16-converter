cmake_minimum_required(VERSION 3.10)

project(utf8-utf16-converter LANGUAGES C)

enable_testing()

if (DEBUG)
    set(CMAKE_C_FLAGS "${CMAKE_C_FLAGS} -O2 -ggdb")
else()
    set(CMAKE_C_FLAGS "${CMAKE_C_FLAGS} -O3")
endif()
set(CMAKE_C_FLAGS "${CMAKE_C_FLAGS} -Wall -Werror -Wextra")

add_subdirectory(converter)
add_subdirectory(tester)
