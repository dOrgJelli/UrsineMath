cmake_minimum_required(VERSION 3.2)

# main project
project(UrsineMath)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11")

# shared source files
set(SHARED_SRC_FILES
    ../Source/SMat3.cpp
    ../Source/SMat3.h
    ../Source/SMat4.cpp
    ../Source/SMat4.h
    ../Source/SQuat.cpp
    ../Source/SQuat.h
    ../Source/SIMD.h
    ../Source/UrsineMath.cpp
    ../Source/UrsineMath.h
    ../Source/UrsineMath.hpp
    ../Source/UrsineTypes.h
    ../Source/Vec2.cpp
    ../Source/Vec2.h
    ../Source/SVec3.cpp
    ../Source/SVec3.h
    ../Source/SVec4.cpp
    ../Source/SVec4.h)

# catch testing suite source files
set(CATCH_SRC_FILES
    ../Dependencies/Testing/catch.hpp)

# test driver source files
set(VECTOR_TEST_SRC_FILES ${SHARED_SRC_FILES} ${CATCH_SRC_FILES}
    VectorLibTests.cpp)

set(MATRIX_TEST_SRC_FILES ${SHARED_SRC_FILES} ${CATCH_SRC_FILES}
    MatrixLibTests.cpp)

# test driver build target
add_executable(UrsineMath-VectorTestDriver ${VECTOR_TEST_SRC_FILES})
add_executable(UrsineMath-MatrixTestDriver ${MATRIX_TEST_SRC_FILES})
