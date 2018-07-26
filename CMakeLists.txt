#1.cmake verson，指定cmake版本 
cmake_minimum_required(VERSION 3.10)

#2.project name，指定项目的名称，一般和项目的文件夹名称对应
PROJECT(warehouse)

include("${PROJECT_SOURCE_DIR}/macro.cmake")


set(CMAKE_ARCHIVE_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/lib)
set(CMAKE_LIBRARY_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/lib)
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/bin)


#find_path(LINGO_PATH NAMES)

find_path(XT_UTILS_PATH NAMES)

#include_directories(${LINGO_PATH}/include)
include_directories(${XT_UTILS_PATH})
#link_directories(${LINGO_PATH}/lib)

#configure_files(${LINGO_PATH}/bin ${CMAKE_RUNTIME_OUTPUT_DIRECTORY}/debug)
#configure_files(${LINGO_PATH}/bin ${CMAKE_RUNTIME_OUTPUT_DIRECTORY}/release)



#6.add executable file，添加要编译的可执行文件
ADD_EXECUTABLE(routing main.cpp)
 
#target_link_libraries(routing Lingd10.lib)

