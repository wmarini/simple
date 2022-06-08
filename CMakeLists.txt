cmake_minimum_required(VERSION 3.16)

project(simple CXX)

set(CMAKE_BUILD_TYPE DEBUG)
set(CMAKE_CXX_STANDARD 20)
set(CMAKE_INCLUDE_CURRENT_DIR ON)
set(CMAKE_CXX_FLAGS "-fconcepts")
#set(CMAKE_EXPORT_COMPILE_COMMANDS ON)

set(SOURCE 
    "src/main.cpp"
    )


MACRO (build_program name)
add_executable(${PROJECT_NAME} ${SOURCE})
TARGET_LINK_LIBRARIES( ${PROJECT_NAME} )
ENDMACRO()

build_program(simple)
