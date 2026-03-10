cmake_minimum_required(VERSION 3.4...3.28 FATAL_ERROR)

project(imgui)

file(GLOB_RECURSE source_files
	"./imgui.cpp"
	"./imgui.h"
	"./imconfig.h"
	"./imgui_demo.cpp"
	"./imgui_draw.cpp"
	"./imgui_internal.h"
	"./imgui_tables.cpp"
	"./imgui_widgets.cpp"
	"./imstb_rectpack.h"
	"./imstb_textedit.h"
	"./imstb_truetype.h"

	"./backends/imgui_impl_glfw.cpp"
	"./backends/imgui_impl_glfw.h"
	"./backends/imgui_impl_opengl3.cpp"
	"./backends/imgui_impl_opengl3.h"
)

add_library(imgui ${source_files})

# imgui expects GLFW to exists next to it
target_include_directories(imgui PUBLIC ../glfw/glfw/include ./imgui/backends/ ./imgui)
