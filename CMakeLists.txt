cmake_minimum_required(VERSION 3.13)

# ***************************************************************
set(CTGT hellogtest)
project(${CTGT})
# ***************************************************************

# ---------------------------------------------------------------
# Current Target executable
add_executable(${CTGT}
    src/hellogtest.cpp
)

# ---------------------------------------------------------------
# all the following is necessary for testing...
include(CTest)
enable_testing()

# This is necessary to use cmake_addons. It is assumed that
# cmake_addons component is placed in the base directory of the
# project inside the cmake_addons directory (e.g. using a
# git submodule)
# Find cmake_addons at: https://github.com/fpiantini/cmake_addons
set(cmakeAddonsDir "${CMAKE_CURRENT_SOURCE_DIR}/cmake_addons")

# Add gtest/gmock support
include(${cmakeAddonsDir}/addgtestsupport.cmake)

target_compile_options(${CTGT} PRIVATE -Werror)
target_compile_features(${CTGT} PRIVATE cxx_std_11)

target_link_libraries(${CTGT} PRIVATE gtest gmock_main)
