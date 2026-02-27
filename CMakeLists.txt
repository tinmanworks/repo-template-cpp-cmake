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

add_library(${PROJECT_NAME}
  src/project_name.cpp
)

target_include_directories(${PROJECT_NAME}
  PUBLIC
    ${CMAKE_CURRENT_SOURCE_DIR}/include
)

if(ENABLE_TESTS)
  enable_testing()
  add_subdirectory(tests)
endif()