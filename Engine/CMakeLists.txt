cmake_minimum_required (VERSION 3.8)

project(Engine)

find_package(SDL2 REQUIRED)
find_package(SDL2_image REQUIRED)
find_package(SDL2_ttf REQUIRED)

set (ENGINE_INCLUDE_DIR "${CMAKE_SOURCE_DIR}/Engine/include")

include_directories(${SDL2_INCLUDE_DIR}
                    ${SDL2_IMAGE_INCLUDE_DIR}
                    ${SDL2_TTF_INCLUDE_DIR}
					${ENGINE_INCLUDE_DIR})

set (ENGINE_SOURCES
		src/engine.cpp
	)

add_library (Engine ${ENGINE_SOURCES})

# Make sure the compiler can find include files for our engine
# when other libraries or executables link to the engine
target_include_directories (Engine PUBLIC ${ENGINE_INCLUDE_DIR})
 