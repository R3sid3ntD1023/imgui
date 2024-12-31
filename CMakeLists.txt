cmake_minimum_required(VERSION 3.8)

file(GLOB_RECURSE SRC CMAKE_CONFIGURE_DEPENDS *.h *.cpp)

add_library(ImGui STATIC ${SRC})
set_property(TARGET ImGui PROPERTY CXX_STANDARD 20)
