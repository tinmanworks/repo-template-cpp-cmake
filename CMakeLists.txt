cmake_minimum_required(VERSION 3.20)

project(ProjectName
  VERSION 0.1.0
  DESCRIPTION "Project description"
  LANGUAGES CXX
)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)

option(ENABLE_TESTS "Enable tests" ON)
option(BUILD_APPS "Build example applications" ON)

add_library(
  src/project_name.cpp
)

target_include_directories(
  PUBLIC
    /include
)

if(BUILD_APPS)
  add_executable(_cli
    apps/project_name_cli.cpp
  )
  target_link_libraries(_cli
    PRIVATE 
  )
endif()

if(ENABLE_TESTS)
  enable_testing()
  add_subdirectory(tests)
endif()
