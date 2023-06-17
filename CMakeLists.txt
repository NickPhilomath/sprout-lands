cmake_minimum_required(VERSION 3.26)

set(CXX_STANDARD 17)
set(CXX_STANDARD_REQUIRED ON)

project(sprout-lands VERSION 1.0)

file(GLOB_RECURSE SRC_FILES src/*.cpp)
add_executable(sprout-lands main.cpp ${SRC_FILES} ${ENET_FILES})
target_include_directories(sprout-lands PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/include)