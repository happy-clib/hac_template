# clib-template

![version](https://img.shields.io/badge/version-1.0.0-7446ff)

A **C** library project template based on [CMake](https://cmake.org/).

## Directory tree

```shell
root/
  |-- src/
    |-- sum.h # sample header file
    |-- sum.c # sample source file
    |-- CMakeLists.txt # for building shared libraries
  |-- test/
    |-- test.c # define unit test cases
    |-- CMakeLists.txt # for building and running unit test
  |-- fuzz/
    |-- CMakeLists.txt # for building and running fuzz test
  |-- ...
```

## Installation

> This template uses `CMake` and `make` to build and install libraries.

```shell
# Create output dir
mkdir build && cd build

# Configure CMake
cmake .. \
  -DCMAKE_C_COMPILER=gcc \ # choose a c compiler
  -DCMAKE_INSTALL_PREFIX=/usr \ # target install directory path prefix
  -DCMAKE_BUILD_TYPE=Release 

# Install
sudo cmake --install . 
```

After installation, the header files are in the `/usr/include/sum` while the static and dynamic libraries are in the `/usr/lib`.

## Usage

> The following is sample code usage description:

```c
#include <stdio.h>
#include "sum/sum.h"

int main() {
  printf("%d\n", sum(1, 2));
  return 0;
}
```

## API

> The following is sample code API description:

### `int sum(int a, int b)`

Calculate two `integer`s sum.


## Workflows

|workflow|trigger|tasks|
|----|-----|----|
|[pr.yml](/.github/workflows/pr.yml)|pull requests or new push to `main`|check building and unit test across platforms|


## CHANGELOG

TODO
