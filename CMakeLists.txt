cmake_minimum_required(VERSION 3.16)

project(Systray LANGUAGES CXX)

# Require C++17 or newer for Qt 6
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

# Instruct CMake to run moc automatically when needed.
set(CMAKE_AUTOMOC ON)
set(CMAKE_AUTORCC ON)
set(CMAKE_AUTOUIC ON)

# Find Qt 6 components
find_package(Qt6 REQUIRED COMPONENTS Widgets Svg)

# Tell CMake to create the helloworld executable
add_executable(Systray
    WIN32
    main.cpp
    window.cpp
    systray.qrc
    Readme.md
)

# Use the Widgets module from Qt 5.
target_link_libraries(Systray PRIVATE
    Qt6::Widgets
    Qt6::Svg
)
