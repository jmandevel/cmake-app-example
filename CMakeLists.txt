# this line is required at start of your top level CMakeLists.txt file
# use the command cmake --version to retrieve the version of CMake you have installed
# https://cmake.org/cmake/help/latest/command/cmake_minimum_required.html
cmake_minimum_required(VERSION 3.13)

# define your project where all your targets will be attached to
# targets include executable and library binaries you want to build
# https://cmake.org/cmake/help/latest/command/project.html
project(MyProject
# all fields below are optional
# provide a short description of your project
    DESCRIPTION "This is a simple CMake project example"
# define the version of your project
# https://semver.org/
    VERSION 0.0.0.0 
# list all languages you want to compile in your project
    LANGUAGES C CXX
)

# set some variable values
# change this to the version of C++ you want to support
set(CMAKE_CXX_STANDARD 17) 
set(CMAKE_CXX_STANDARD_REQUIRED True)

# define an executable target to build from source files
# you could also add source files here directly instead of using target_sources() later
# https://cmake.org/cmake/help/latest/command/add_executable.html
add_executable(MyApp)

# execute the CMakeLists.txt file in the src/ subdirectory
add_subdirectory(src)

# specify include directories for the MyApp target
# so that header files can be found during compilation
# https://cmake.org/cmake/help/latest/command/target_include_directories.html
target_include_directories(
    MyApp
    PRIVATE
        ${PROJECT_SOURCE_DIR}/src
        ${PROJECT_SOURCE_DIR}/include   
)