cmake_minimum_required(VERSION 3.8)

file(GLOB_RECURSE SRC CMAKE_CONFIGURE_DEPENDS include/** src/**)

add_library(glad STATIC ${SRC})
target_include_directories(glad PUBLIC ${CMAKE_CURRENT_LIST_DIR}/include)
