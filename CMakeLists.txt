cmake_minimum_required(VERSION 4.5 FATAL_ERROR)

set(CMAKE_CXX_STANDARD 26)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)
set(CMAKE_EXPORT_COMPILE_COMMANDS ON)

project(dispatchbm LANGUAGES CXX)

add_subdirectory(libbench)
add_subdirectory(mark)

execute_process(COMMAND ${CMAKE_COMMAND} -E create_symlink
     ${CMAKE_BINARY_DIR}/compile_commands.json
     ${CMAKE_SOURCE_DIR}/compile_commands.json
)
