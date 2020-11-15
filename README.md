# hellogtest
A C++ minimal setup to play with gtest/gmock

Uses CMake for project and build management.

Uses the CMake gtest/gmock support provided in the `cmake_addons` repo (https://github.com/fpiantini/cmake_addons).

To build:

```bash
mkdir build
cd build
cmake ..
cmake -G "<your_preferred_build_system>" .
cmake --build .
```

The `cmake -G <...>` command is necessary only if you want to change the default build system. To check the build system available in your system (and the default one) use the following command:

```bash
cmake -G
```
