

cmake_minimum_required(VERSION 3.13)
project(SUBDIRECTORIES)


add_executable(${PROJECT_NAME} main.cpp)

add_subdirectory(Maths)
target_include_directories(${PROJECT_NAME} PUBLIC Maths)
target_link_libraries(${PROJECT_NAME} maths)