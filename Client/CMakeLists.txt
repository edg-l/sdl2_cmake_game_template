cmake_minimum_required (VERSION 3.8)

project(Client)

find_package(SDL2 REQUIRED)
find_package(SDL2_image REQUIRED)
find_package(SDL2_ttf REQUIRED)

include_directories(${SDL2_INCLUDE_DIR}
                    ${SDL2_IMAGE_INCLUDE_DIR}
                    ${SDL2_TTF_INCLUDE_DIR})

set (CLIENT_SOURCES
        "src/client.cpp")

add_executable (Client ${CLIENT_SOURCES})

# LINK_PUBLIC to use Engine includes
target_link_libraries(Client LINK_PUBLIC
							${SDL2_LIBRARY}
                            ${SDL2_IMAGE_LIBRARIES}
                            ${SDL2_TTF_LIBRARIES}
							Engine)
 