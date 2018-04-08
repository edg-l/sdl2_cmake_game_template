cmake_minimum_required (VERSION 3.8)

project ("Server")

set (SERVER_SOURCES
        "src/server.cpp")

add_executable (Server ${SERVER_SOURCES})
 
 target_link_libraries(Server LINK_PUBLIC Engine)