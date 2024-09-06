# CMakeLists.txt
cmake_minimum_required(VERSION 3.15)
project(cpp_template)

message("CMAKE_BINARY_DIR=${CMAKE_BINARY_DIR}")
message("CMAKE_HOME_DIRECTORY=${CMAKE_HOME_DIRECTORY}")
message("CMAKE_CONFIGURATION_TYPES=${CMAKE_CONFIGURATION_TYPES}")

# (Globally) find dependencies provided by vcpkg (via vcpkg.cmake)
find_package(fmt CONFIG REQUIRED)

# main target
add_subdirectory(src/example_app)

enable_testing()
# tests target
add_subdirectory(src/example_test)
