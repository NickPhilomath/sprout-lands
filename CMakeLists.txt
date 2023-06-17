cmake_minimum_required(VERSION 3.26)

set(CXX_STANDARD 17)
set(CXX_STANDARD_REQUIRED ON)

project(sprout-lands VERSION 1.0)

# look for sfml
set(SFML_DIR ${CMAKE_CURRENT_SOURCE_DIR}/libs/SFML-2.5.1/lib/cmake/SFML)
find_package(SFML 2.5 COMPONENTS audio graphics window system REQUIRED)

file(GLOB_RECURSE SRC_FILES src/*.cpp)
add_executable(sprout-lands main.cpp ${SRC_FILES})
target_include_directories(sprout-lands PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/include)
target_include_directories(sprout-lands PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/libs/SFML-2.5.1/include)
# target_include_directories(sprout-lands PUBLIC ${SFML_INCLUDE_DIR})
# target_link_libraries(sprout-lands PUBLIC ${SFML_LIBRARIES} ${SFML_DEPENDENCIES})
target_link_libraries(sprout-lands PUBLIC sfml-graphics)