cmake_minimum_required(VERSION 3.22)
project(my_project VERSION 1.0)


set(Tutorial_VERSION_MAJOR 1)
set(Tutorial_VERSION_MINOR 0)


set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED True)

configure_file(TutorialConfig.h.in
 TutorialConfig.h
              )

add_executable(Tutorial tutorial.cxx)
target_include_directories(Tutorial PUBLIC
                            "${PROJECT_BINARY_DIR}"
                            )               
