# clib-template

![version](https://img.shields.io/badge/version-1.0.0-7446ff)

A **C** library project template based on [CMake](https://cmake.org/).

## Installation

```shell
# Configure CMake
cmake \
  -S . \
  -DCMAKE_C_COMPILER=gcc \ # choose a c compiler
  -DCMAKE_INSTALL_PREFIX=/usr \ # target install directory path prefix
  -DCMAKE_BUILD_TYPE=Release 

# Install
sudo make install
```

After installation, the header files are in `/usr/include/sum` while the static and dynamic libraries are in the `/usr/lib`.

## Usage

```c
#include <stdio.h>
#include "sum/sum.h"

int main() {
  printf("%d\n", sum(1, 2));
  return 0;
}
```

## API

### `int sum(int a, int b)`

Calculate two `integer`s sum.


## Workflows

|workflow|trigger|tasks|
|----|-----|----|
|[pr.yml](/.github/workflows/pr.yml)|pull requests or new push to `main`|check compiling and unit test|


## CHANGELOG

TODO
