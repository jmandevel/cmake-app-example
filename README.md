# CMake App Example

This is a simple example of a C++ project built with CMake.

## Prerequisites

-   [CMake](https://cmake.org/download/) (version 3.10 or higher)
-   A C++ Compiler (GCC, Clang, MSVC, etc.)
-   [Visual Studio Code](https://code.visualstudio.com/) (optional)
-   [CMake Tools Extension](https://marketplace.visualstudio.com/items?itemName=ms-vscode.cmake-tools) for VS Code (optional)

## Building with Command Line (without VS Code)

1.  Create a build directory:
    ```bash
    mkdir build
    ```

2. Enter the build directory:
    ````bash
    cd build
    ````

3.  Configure the project:
    ```bash
    cmake ..
    ```

4.  Build the executable:
    ```bash
    cmake --build .
    ```

5.  Run the application:
    -   On Windows: `.\Debug\CMakeAppExample.exe` (or `.\CMakeAppExample.exe` depending on generator)
    -   On Linux/macOS: `./CMakeAppExample`

NOTE: You can combine steps 1 and 3 into one command by using this from the root directory of your project:

```bash
cmake -S . -B ./build/
```

## Building with VS Code (CMake Tools)

1.  Open the project folder in VS Code.

2.  **Select a Kit**:
    -   Open the Command Palette (`Ctrl+Shift+P` or `Cmd+Shift+P`).
    -   Type `CMake: Select a Kit` and choose your compiler (e.g., GCC, Clang, Visual Studio).

3.  **Configure**:
    -   The project should configure automatically when you select a kit.
    -   If not, run `CMake: Configure` from the Command Palette.

4.  **Build**:
    -  Run `CMake: Build` from the Command Palette to build.
    - For debugging, run `CMake: Debug` from the command palette.

You may find it easier to control CMakeTools from the menu instead. A button for it should appear on the left sidebar of VSCode. If you don't see it, restart VSCode and it should appear.