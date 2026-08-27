cmake_minimum_required(VERSION 3.20)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

project(
    brevm
    VERSION 0.0.2
    LANGUAGES CXX
)

file(GLOB_RECURSE SOURCES
    "${CMAKE_SOURCE_DIR}/src/*.cpp"
)

add_executable(brevm ${SOURCES})

target_include_directories(brevm PRIVATE
    "${CMAKE_SOURCE_DIR}"
    ${CMAKE_CURRENT_SOURCE_DIR}/include
    ${CMAKE_CURRENT_SOURCE_DIR}/depends/brevm-reference
)

