cmake_minimum_required(VERSION 3.7)
project(OpenGLPractice)

set(CMAKE_CXX_STANDARD 14)

set(SOURCE_FILES main.cpp)

find_package(OpenGL REQUIRED)
find_package(GLUT REQUIRED)
include_directories(${OPENGL_INCLUDE_DIR} ${GLUT_INCLUDE_DIR})

message([OpenGL] ${OPENGL_INCLUDE_DIR})
message([GLUT] ${GLUT_INCLUDE_DIR})

add_executable(OpenGLPractice ${SOURCE_FILES})

target_link_libraries(OpenGLPractice ${GLUT_INCLUDE_DIR} ${OPENGL_INCLUDE_DIR})
