# hellogtest
A C++ minimal setup to play with gtest/gmock

Uses CMake for project and build management.

Uses the CMake gtest/gmock support provided in the `cmake_addons` repo (https://github.com/fpiantini/cmake_addons). The `cmake_addons` is used as a submodule, so after a fresh clone enter the following command:

```bash
git submodule update --init --recursive
```

The gtest/gmock libraries are built inside this project, so it is not necessary to install them on the PC used for development.

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

To check the tests, enter the following command in the `build` directory:

```bash
./hellogtest
```

