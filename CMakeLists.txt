# CMakeList.txt: archivo del proyecto de CMake de nivel superior, establezca la configuración global
# e incluya los subproyectos aquí.
#
cmake_minimum_required (VERSION 3.8)

set (CMAKE_MODULE_PATH ${CMAKE_MODULE_PATH} "${CMAKE_SOURCE_DIR}/cmake/")
 
project ("MyGame")

# Incluya los subproyectos.
add_subdirectory ("Engine")
add_subdirectory ("Client")
add_subdirectory ("Server")
