cmake_minimum_required(VERSION 3.2)
project(Testing)

# Build 2 executables:passing and failing
add_executable(passing passing.cpp)
add_executable(failing failing.cpp)

# Define 2 tests, one for each executable.
enable_testing()
add_test(NAME passing COMMAND passing)
add_test(NAME failing COMMAND failing)

# Failing will fail, mark at as an expected failure
set_property(TEST failing 
 PROPERTY WILL_FAIL TRUE
)
