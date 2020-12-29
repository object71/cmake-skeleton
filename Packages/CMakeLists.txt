project(Packages)

add_subdirectory(raylib)

add_library(Packages STATIC include/Packages.h src/Packages.cpp)

target_link_libraries(Packages raylib)

target_include_directories(Packages
                           PUBLIC
                           $<INSTALL_INTERFACE:include>
                           $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}/include>
                           PRIVATE
                           ${CMAKE_CURRENT_SOURCE_DIR}/src
                           )