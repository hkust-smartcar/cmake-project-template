# HKUST Smart Car Libsccc CMake Template

This project template for a CMake environment is capable of compiling Smart Car projects. This template is compatible with Jetbrain's CLion IDE, though further setup is required to debug and flash within CLion.

## Setup

1. Setup the ARM toolchain in system environment variables, as the paths will be searched by CMake to find the ARM compiler and such.

2. Use `toolchain_arm_none_eabi_gcc.cmake` as custom CMake toolchain. To do so in CLion, go to **Settings > Build, Execution, Deployment > CMake options** and paste in the following:

  ```shell
  -DCMAKE_TOOLCHAIN_FILE=toolchain_arm_none_eabi_gcc.cmake
  ```

3. Retrieve a copy of the linker scripts, e.g. `d10.ld`, `f15.ld`, etc and place them in `build/`.

4. Edit the suggested sections in `CMakeLists.txt`.

