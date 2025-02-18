cmake_minimum_required(VERSION 3.10)
project(openGLApp)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

# Include GLFW headers
include_directories(${PROJECT_SOURCE_DIR}/include)

# Include source files
set(SRC_DIR ${PROJECT_SOURCE_DIR}/src)

# Recursively collect all source files
file(GLOB_RECURSE SOURCES ${SRC_DIR}/*.cpp ${SRC_DIR}/*.c)
file(GLOB_RECURSE HEADERS ${SRC_DIR}/*.h ${SRC_DIR}/*.hpp)

# Add the executable
# add_executable(${PROJECT_NAME} glad.c framework.cpp framework.h lodepng.cpp lodepng.h GreenTriangleNaked.cpp)
add_executable(${PROJECT_NAME} ${SOURCES} ${HEADERS})
# Link the static GLFW library
target_link_libraries(${PROJECT_NAME} ${PROJECT_SOURCE_DIR}/lib/libglfw3.a)

# Link math library
target_link_libraries(${PROJECT_NAME} m)

# Copy the glfw3.dll to the output directory (same as the executable)
add_custom_command(TARGET ${PROJECT_NAME} POST_BUILD
    COMMAND ${CMAKE_COMMAND} -E copy
    ${PROJECT_SOURCE_DIR}/lib/glfw3.dll
    $<TARGET_FILE_DIR:${PROJECT_NAME}>)