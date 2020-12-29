project(Main LANGUAGES CXX)

add_executable(Main
               src/Main.cpp
               src/Main.h
               )

target_link_libraries(Main PRIVATE Packages)