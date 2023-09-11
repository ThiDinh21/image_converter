cmake_minimum_required(VERSION 3.22)

# Option for precompiled headers
if (${CMAKE_VERSION} VERSION_GREATER_EQUAL "3.22.0")
  option(USE_PCH "Use precompiled headers" ON)
endif()

project(ImageConverter)

set(CMAKE_PREFIX_PATH "C:/QT_new/6.5.2/msvc2019_64")


# Find the QtWidgets package from Qt6
find_package(Qt6 COMPONENTS Core Gui Widgets Quick REQUIRED)

# Potentially set any global configurations or properties here

add_subdirectory(TUI)
add_subdirectory(GUI)
