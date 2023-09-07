cmake_minimum_required(VERSION 3.21)

add_library(
    ImGui
    imgui.cpp
    imgui_draw.cpp
    imgui_tables.cpp
    imgui_widgets.cpp
    imgui_demo.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/misc/freetype/imgui_freetype.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/backends/imgui_impl_opengl3.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/backends/imgui_impl_glfw.cpp
)

target_include_directories(ImGui PUBLIC
    ${CMAKE_CURRENT_SOURCE_DIR}
    ${CMAKE_CURRENT_SOURCE_DIR}/backends
    ${CMAKE_CURRENT_SOURCE_DIR}/misc/freetype
    ${CMAKE_CURRENT_SOURCE_DIR}/examples/libs/glfw/include
)