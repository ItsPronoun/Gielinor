cmake_minimum_required(VERSION 3.12.0)
project(Gielinor VERSION 0.1.0)

add_executable(Gielinor)

find_package(Python3 COMPONENTS Interpreter Development)

target_link_libraries(Gielinor PRIVATE ${Python3_LIBRARIES})
target_include_directories(Gielinor PRIVATE ${Python3_INCLUDE_DIRS})

add_subdirectory(src)