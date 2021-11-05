# Set the required cmake version
cmake_minimum_required(VERSION 3.10)

# Set the project name, version, and languages
project(yocto_test_app VERSION 1.0 LANGUAGES C CXX)

# Set the target name
set(TARGET_NAME "yocto_test_app")

# Set output directories
set(CMAKE_ARCHIVE_OUTPUT_DIRECTORY ${CMAKE_SOURCE_DIR}/output)
set(CMAKE_LIBRARY_OUTPUT_DIRECTORY ${CMAKE_SOURCE_DIR}/output)
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_SOURCE_DIR}/output)

# Create a source list
set(SOURCES ${CMAKE_SOURCE_DIR}/src/main.c)

# Create an executable
add_executable(${TARGET_NAME} ${SOURCES})

# Add an additional property that will delete compile binaires on a "clean" command
set_property(DIRECTORY APPEND PROPERTY ADDITIONAL_MAKE_CLEAN_FILES "output")
