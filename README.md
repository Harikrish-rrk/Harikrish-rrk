### Hi there 👋



Here are some common CMake CLI (Command Line Interface) commands used in typical workflows:

# 1. Generate Build Files
Generate build files using a CMake generator (e.g., Makefile, Ninja, Visual Studio):

```cmake -S <source_directory> -B <build_directory> -G <generator_name>```
-S: Specify the source directory containing the CMakeLists.txt.
-B: Specify the build directory where the build files will be generated.
-G: Specify the generator (e.g., "Unix Makefiles", "Ninja", "Visual Studio 16 2019").
Example:

```cmake -S . -B build -G "Unix Makefiles"```

# 2. Configure a Project
Set CMake variables during configuration:

```cmake -S <source_directory> -B <build_directory> -D<variable>=<value> -D<variable>=<value>: ```

Define a CMake variable. You can define multiple variables by adding more -D flags.
Example:

```cmake -S . -B build -DCMAKE_BUILD_TYPE=Release -DBUILD_SHARED_LIBS=ON```

# 3. Build a Project
Build the project after configuration:

```cmake --build <build_directory> --target <target_name> --config <configuration>```
--target: Specify a particular target to build (optional).
--config: Specify the build configuration (e.g., Debug, Release).

Example:

```cmake --build build --config Release```
# 4. Install the Project
Install the build outputs to a specified directory:

```cmake --install <build_directory> --prefix <install_directory>```

Example:

```cmake --install build --prefix /usr/local```

# 5. Run Tests
Run tests after building the project:


```ctest --test-dir <build_directory> --output-on-failure```
--output-on-failure: Shows test output if a test fails.
Example:

```ctest --test-dir build --output-on-failure```

# 6. Clean the Build Directory
Remove build artifacts:

```cmake --build <build_directory> --target clean```

Example:

```cmake --build build --target clean```

# 7. Package the Project
Create a package (e.g., .tar.gz, .zip) from the build artifacts:

```cpack --config <package_configuration_file>```

Example:
```cpack --config CPackConfig.cmake```
These commands help manage a CMake-based project through the command line, from generation and building to testing and packaging.

