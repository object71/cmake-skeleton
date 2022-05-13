project(Packages)

add_subdirectory(raylib)

add_library(Packages INTERFACE)
target_link_libraries(Packages INTERFACE raylib)