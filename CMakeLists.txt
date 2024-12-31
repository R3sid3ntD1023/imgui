cmake_minimum_required(VERSION 3.8)

file(GLOB_RECURSE IMGUI_SRC CMAKE_CONFIGURE_DEPENDS *.h *.cpp misc/cpp/*)

add_library(imgui STATIC ${IMGUI_SRC})
set_property(TARGET imgui PROPERTY CXX_STANDARD 20)
