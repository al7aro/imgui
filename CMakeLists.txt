cmake_minimum_required(VERSION 3.25.0)
project(imgui)

file(GLOB_RECURSE source_files
	"./*.cpp"
	"./*.h"

	"./backends/imgui_impl_glfw.cpp"
	"./backends/imgui_impl_glfw.h"
	"./backends/imgui_impl_opengl3.cpp"
	"./backends/imgui_impl_opengl3.h"
)

add_library(imgui ${source_files})

target_include_directories(imgui PUBLIC backends/ ./)
