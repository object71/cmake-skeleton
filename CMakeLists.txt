cmake_minimum_required(VERSION 3.16)

project(CmakeSkeleton)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

if(WIN32)
    add_compile_definitions(WINDOWS=1)
endif ()

if (UNIX AND NOT APPLE)
    add_compile_definitions(LINUX=1)
endif ()

if (APPLE)
    add_compile_definitions(APPLE=1)
endif ()

if(${CMAKE_BUILD_TYPE} MATCHES Debug)
    add_compile_definitions(_DEBUG=1)
else()
    add_compile_definitions(NDEBUG=1)
endif(${CMAKE_BUILD_TYPE} MATCHES Debug)

add_subdirectory(Packages)
add_subdirectory(Main)