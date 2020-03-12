cmake_minimum_required(VERSION 3.7)

project(xxxgamexxx)

find_package(SDL2 REQUIRED)


add_executable(main src/main.cpp)

if (DEFINED ${SDL2_INCLUDE_DIRS})
    include_directories(${SDL2_INCLUDE_DIRS})
    target_link_libraries(main ${SDL2_INCLUDE_DIRS})
else()
    target_link_libraries(main SDL2::SDL2)
endif()
