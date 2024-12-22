cmake_minimum_required(VERSION 3.8)

file(GLOB IMGUI_SRC CMAKE_CONFIGURE_DEPENDS *.h *.cpp misc/cpp/*.cpp)

add_library(imgui STATIC ${IMGUI_SRC})
set_target_properties(imgui PROPERTIES
	CMAKE_CXX_STANDARD 20
)

target_include_directories(imgui PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})
target_include_directories(imgui PUBLIC ../${CMAKE_CURRENT_SOURCE_DIR})
target_include_directories(imgui PUBLIC ../${CMAKE_CURRENT_SOURCE_DIR}/backends)
