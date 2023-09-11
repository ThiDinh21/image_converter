set(PROJECT_NAME ImageConverterTUI)

project(ImageConverterConsole)

find_package(Qt6 COMPONENTS Core Quick REQUIRED)

add_executable(${PROJECT_NAME}
    # Your source files here
    main.cpp
    # etc.
)

target_link_libraries(${PROJECT_NAME} PRIVATE Qt6::Core)
