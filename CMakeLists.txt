cmake_minimum_required(VERSION 3.8)

file(GLOB_RECURSE IMGUI_SRC CMAKE_CONFIGURE_DEPENDS include/** src/**)

add_library(imgui STATIC ${IMGUI_SRC})
target_include_directories(imgui PUBLIC ${CMAKE_CURRENT_LIST_DIR}/include)
