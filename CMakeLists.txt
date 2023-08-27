cmake_minimum_required(VERSION 3.14)

project(OpenGL-boilerplate)

# glfw 
set(GLFW_BUILD_DOCS OFF CACHE BOOL "" FORCE)
set(GLFW_BUILD_TESTS OFF CACHE BOOL "" FORCE)
set(GLFW_BUILD_EXAMPLES OFF CACHE BOOL "" FORCE)

add_subdirectory(OpenGL-boilerplate/external/glfw)

target_link_libraries(${PROJECT_NAME} glfw)

# OpenGL
find_package(OpenGL REQUIRED)

target_link_libraries(${PROJECT_NAME} OpenGL::GL)