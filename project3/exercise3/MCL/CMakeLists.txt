cmake_minimum_required(VERSION 2.8 FATAL_ERROR)

add_definitions(-std=c++11)

set(CXX_FLAGS "-Wall")
set(CMAKE_CXX_FLAGS, "${CXX_FLAGS}")
set( CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS}" )

project(MCL)

find_package(PythonLibs REQUIRED)

set(PYTHON_EXECUTABLE "/usr/bin/python2.7")
set(PYTHON_INCLUDE_DIR "/usr/include/python2.7")
set(PYTHON_LIBRARIES "/usr/lib/x86_64-linux-gnu/libpython2.7.so")

include_directories(${PYTHON_INCLUDE_DIRS})
add_executable("${PROJECT_NAME}" solution.cpp)
# add_executable("${PROJECT_NAME}" resampling.cpp)
target_link_libraries("${PROJECT_NAME}" ${PYTHON_LIBRARIES})
