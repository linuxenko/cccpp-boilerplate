# To build components as shared libraries use SHARED keyword
# add_library(ADDLIB SHARED add.cpp)

add_library(ADDLIB add.cpp)

add_executable(CCCPP main.cpp)
target_link_libraries(CCCPP ADDLIB)

