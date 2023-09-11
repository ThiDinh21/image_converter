project(ImageConverterGUI)

# Find necessary Qt modules
find_package(Qt6 COMPONENTS Core Quick REQUIRED)

# Use file(GLOB ...) to automatically pick up new source files in the future
file(GLOB SOURCES
    *.cpp
    *.qml
    *.qrc
)

add_executable(ImageConverterGUI ${SOURCES})

# Link with the required Qt modules
target_link_libraries(ImageConverterGUI PRIVATE Qt6::Core Qt6::Quick)

# Enable QML debugging if required
# target_compile_definitions(ImageConverterGUI PRIVATE QT_QML_DEBUG)
