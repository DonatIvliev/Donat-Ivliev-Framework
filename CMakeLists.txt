cmake_minimum_required(VERSION 3.5)

project(GeometryFramework LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_executable(GeometryFramework main.cpp
    geometry.h geometry.cpp
    point.h point.cpp
    shape.h shape.cpp)

include(GNUInstallDirs)
install(TARGETS GeometryFramework
    LIBRARY DESTINATION ${CMAKE_INSTALL_LIBDIR}
    RUNTIME DESTINATION ${CMAKE_INSTALL_BINDIR}
)
