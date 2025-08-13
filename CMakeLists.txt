cmake_minimum_required(VERSION 3.10)

set(PROJECT_NAME imgui)

option(IMGUI_DEMO "Build imgui_demo.cpp" ON)

set(IMGUI_SOURCES
    ${CMAKE_CURRENT_SOURCE_DIR}/imgui.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/imgui_draw.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/imgui_draw.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/imgui_tables.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/imgui_widgets.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/misc/cpp/imgui_stdlib.cpp
)

if(IMGUI_DEMO)
    list(APPEND IMGUI_SOURCES ${CMAKE_CURRENT_SOURCE_DIR}/imgui_demo.cpp)
endif()

add_library(${PROJECT_NAME} STATIC ${IMGUI_SOURCES}) 
add_library(imgui::imgui ALIAS imgui)
target_compile_definitions(${PROJECT_NAME} PUBLIC _CRT_SECURE_NO_WARNINGS)
target_include_directories(${PROJECT_NAME} PUBLIC "${CMAKE_CURRENT_SOURCE_DIR}" PUBLIC "${CMAKE_CURRENT_SOURCE_DIR}/misc/cpp")
