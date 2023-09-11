project(ImageConverterConsole)

find_package(Qt6 COMPONENTS Core Quick REQUIRED)

add_executable(ImageConverterConsole
    # Your source files here
    main.cpp
    # etc.
)

target_link_libraries(ImageConverterConsole PRIVATE Qt6::Core)
