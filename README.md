### Hi there 👋



Here are some common CMake CLI (Command Line Interface) commands used in typical workflows:

1. Generate Build Files
Generate build files using a CMake generator (e.g., Makefile, Ninja, Visual Studio):

bash
Copy code
cmake -S <source_directory> -B <build_directory> -G <generator_name>
-S: Specify the source directory containing the CMakeLists.txt.
-B: Specify the build directory where the build files will be generated.
-G: Specify the generator (e.g., "Unix Makefiles", "Ninja", "Visual Studio 16 2019").
Example:

```cmake -S . -B build -G "Unix Makefiles"```
2. Configure a Project
Set CMake variables during configuration:
bash
Copy code
cmake -S <source_directory> -B <build_directory> -D<variable>=<value>
-D<variable>=<value>: 

Define a CMake variable. You can define multiple variables by adding more -D flags.
Example:

```cmake -S . -B build -DCMAKE_BUILD_TYPE=Release -DBUILD_SHARED_LIBS=ON```
3. Build a Project
Build the project after configuration:

bash
Copy code
cmake --build <build_directory> --target <target_name> --config <configuration>
--target: Specify a particular target to build (optional).
--config: Specify the build configuration (e.g., Debug, Release).
Example:

```cmake --build build --config Release```
4. Install the Project
Install the build outputs to a specified directory:

bash
Copy code
cmake --install <build_directory> --prefix <install_directory>
--prefix: Specify the directory to install the outputs (optional, if not set, it will install to the default location).
Example:

```cmake --install build --prefix /usr/local```

5. Run Tests
Run tests after building the project:

bash
Copy code
ctest --test-dir <build_directory> --output-on-failure
--output-on-failure: Shows test output if a test fails.
Example:

bash
Copy code
ctest --test-dir build --output-on-failure
6. Clean the Build Directory
Remove build artifacts:

bash
Copy code
cmake --build <build_directory> --target clean
Example:

bash
Copy code
cmake --build build --target clean
7. Package the Project
Create a package (e.g., .tar.gz, .zip) from the build artifacts:

bash
Copy code
cpack --config <package_configuration_file>
Example:

bash
Copy code
cpack --config CPackConfig.cmake
These commands help manage a CMake-based project through the command line, from generation and building to testing and packaging.

<!--
**Harikrish-rrk/Harikrish-rrk** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
