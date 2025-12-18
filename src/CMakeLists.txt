# include source files for the MyApp target
# https://cmake.org/cmake/help/latest/command/target_sources.html
target_sources(
    MyApp
    PRIVATE
        "main.cpp"
        # you can add more source files here as needed
        # then you need to reconfigure and rebuild your project
        # to reconfigure, delete the build folder and then rerun cmake
)