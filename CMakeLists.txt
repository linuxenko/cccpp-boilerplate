project(CCCPP)

cmake_minimum_required(VERSION 2.8)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

if ($ENV{RELEASE})
  set (CMAKE_CXX_FLAGS "-O2 -Wall")
else()
  set (CMAKE_CXX_FLAGS "-g -Wall")
endif()

if ($ENV{TRAVIS})
  message(STATUS "Travis-CI build.")
else()
  message(STATUS "Local build")
endif()

include_directories("${PROJECT_SOURCE_DIR}/include")

# Cmake wrapper does not work properly with tests
# enable_testing()

add_subdirectory(${PROJECT_SOURCE_DIR}/src)
add_subdirectory(${PROJECT_SOURCE_DIR}/tests)