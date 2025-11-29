cmake_minimum_required(VERSION 3.10)
project(HelloWorld C)

# Set C standard
set(CMAKE_C_STANDARD 99)
set(CMAKE_C_STANDARD_REQUIRED ON)

# Add executable
add_executable(hello_world src/main.c)

# Set output directory
set_target_properties(hello_world PROPERTIES
    RUNTIME_OUTPUT_DIRECTORY "${CMAKE_BINARY_DIR}/bin"
)

# Install target
install(TARGETS hello_world DESTINATION bin)
