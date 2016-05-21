cmake_minimum_required(VERSION 2.8.11)

project(Systray)

# Find includes in corresponding build directories
set(CMAKE_INCLUDE_CURRENT_DIR ON)
# Instruct CMake to run moc automatically when needed.
set(CMAKE_AUTOMOC ON)
set(CMAKE_AUTORCC ON)
SET(QT_USE_QTSVG 1)

# Find the QtWidgets library
find_package(Qt5Widgets)
find_package(Qt5Svg REQUIRED)
include(FeatureSummary)
feature_summary(WHAT ALL INCLUDE_QUIET_PACKAGES FATAL_ON_MISSING_REQUIRED_PACKAGES)

# Tell CMake to create the helloworld executable
add_executable(Systray WIN32 main.cpp window.cpp systray.qrc)

# Use the Widgets module from Qt 5.
target_link_libraries(Systray Qt5::Widgets Qt5::Svg)
