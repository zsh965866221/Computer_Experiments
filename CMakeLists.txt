cmake_minimum_required(VERSION 3.9)
project(Computer_Experiments)

set(CMAKE_CXX_STANDARD 11)

SET(EXECUTABLE_OUTPUT_PATH ${PROJECT_SOURCE_DIR}/out)
SET(LIBRARY_OUTPUT_PATH ${PROJECT_SOURCE_DIR}/out)

set(CMAKE_DEBUG_POSTFIX "_d")
set(CMAKE_RELEASE_POSTFIX "_r")

set_target_properties(${TARGET_NAME} PROPERTIES DEBUG_POSTFIX "_d")
set_target_properties(${TARGET_NAME} PROPERTIES RELEASE_POSTFIX "_r")

add_executable(main main.cpp)

## ----------------------------------------------------------------------
add_library(add SHARED test/add.c)
add_executable(addtest test/addtest.c)
target_link_libraries(addtest add)


