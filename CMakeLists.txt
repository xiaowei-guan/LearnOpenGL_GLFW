cmake_minimum_required(VERSION 3.28.3)
project(LearnOpenGL VERSION 0.1.0 LANGUAGES C CXX)

find_package(PkgConfig REQUIRED)
pkg_check_modules(GLFW REQUIRED glfw3)
message(STATUS "Found GLFW3 in ${GLFW_INCLUDE_DIRS}")

include_directories(
    $(GLFW_INCLUDE_DIRS)
)

add_executable(LearnOpenGL main.cpp)

target_link_libraries(LearnOpenGL ${GLFW_LIBRARIES})

