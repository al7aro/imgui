cmake_minimum_required(VERSION 3.25.0)
project(imgui)

add_library(imgui

	"./*.cpp"
	"./*.h"

	"./backends/imgui_impl_glfw.cpp"
	"./backends/imgui_impl_glfw.h"
	"./backends/imgui_impl_opengl3.cpp"
	"./backends/imgui_impl_opengl3.h"
)

target_include_directories(imgui PUBLIC backends/ ./)