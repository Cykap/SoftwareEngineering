cmake_minimum_required(VERSION 3.10)

# set the project name
project(HelloProj VERSION 1.0)
<<<<<<< HEAD

# specify the C++ standard
# use the CMAKE_CXX_STANDARD variable
set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED TRUE)

#export configuration to source code
configure_file(cmake/HelloProjConfig.h.in HelloProjConfig.h)

#add executable
option(HELLOWORD_WITH_EXECUTABLES "Compile mains" ON)
if(HELLOWORD_WITH_EXECUTABLES)
 message(STATUS "Configuring Hello World with executables")
 add_subdirectory(mains)
endif()

=======
#export configuration to source code
configure_file(HelloProjConfig.h.in HelloProjConfig.h)
#add the executable target named HelloWorld
add_executable(HelloWorld hello.cpp)

# add binary tree to the list of paths to search includes
target_include_directories(HelloWorld 
	PUBLIC "${PROJECT_BINARY_DIR}")
>>>>>>> 4255be46e1236e3591d329a57aae5fd34ca6618c
