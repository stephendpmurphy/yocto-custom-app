# Set the required cmake version
cmake_minimum_required(VERSION 3.10)

# Set the project name, version, and languages
project(yocto_test VERSION 1.0 LANGUAGES C CXX)

# Create an executable
add_executable(yocto-test-app ${CMAKE_SOURCE_DIR}/src/main.c)

# Add an install instruction
install(TARGETS yocto-test-app RUNTIME DESTINATION bin)
