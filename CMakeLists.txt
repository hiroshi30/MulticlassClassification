cmake_minimum_required(VERSION 3.28 FATAL_ERROR)

project(MulticlassClassification
	VERSION 0.0.1
	DESCRIPTION ""
	LANGUAGES C
)


# kazamori
add_subdirectory(kazamori)


# GUI
add_subdirectory(GUI)


# MulticlassClassification
add_executable(main)

target_sources(main PRIVATE
	src/main.c
)

target_include_directories(main PRIVATE
    kazamori
    GUI
)

target_link_libraries(main PRIVATE
    kazamori
    GUI
)

if (CMAKE_BUILD_TYPE STREQUAL "Release")
	# -mwindows - remove console output
	message("++ main.exe built with -mwindows")
	target_compile_options(main PRIVATE -mwindows)
endif()
target_compile_options(main PRIVATE -Wall -Wextra -Wpedantic -D${CMAKE_BUILD_TYPE})
target_compile_features(main PRIVATE c_std_23)
