set(PROJECT_NAME ImageConverterGUI)

set(CMAKE_AUTOUIC ON)
set(CMAKE_AUTOMOC ON)
set(CMAKE_AUTORCC ON)

project(${PROJECT_NAME})

# Find necessary Qt modules
find_package(Qt6 COMPONENTS Core Quick REQUIRED)

# # Use file(GLOB ...) to automatically pick up new source files in the future
# file(GLOB SOURCES
#     *.cpp
#     *.qml
#     *.qrc
# )

add_executable(${PROJECT_NAME} ${SOURCES} main.qml main.cpp qml.qrc)

set_target_properties(${PROJECT_NAME} PROPERTIES AUTORCC ON)

# Link with the required Qt modules
target_link_libraries(${PROJECT_NAME} PRIVATE Qt6::Core Qt6::Quick)

# Enable QML debugging if required
# target_compile_definitions(ImageConverterGUI PRIVATE QT_QML_DEBUG)