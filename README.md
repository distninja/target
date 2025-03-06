# target

[![Build Status](https://github.com/distninja/target/workflows/ci/badge.svg?branch=main&event=push)](https://github.com/distninja/target/actions?query=workflow%3Aci)
[![codecov](https://codecov.io/gh/distninja/target/branch/main/graph/badge.svg?token=t31YICk0ek)](https://codecov.io/gh/distninja/target)
[![License](https://img.shields.io/github/license/distninja/target.svg)](https://github.com/distninja/target/blob/main/LICENSE)
[![Tag](https://img.shields.io/github/tag/distninja/target.svg)](https://github.com/distninja/target/tags)



## Introduction

*target* is the ninja target of [distninja](https://github.com/distninja) written in Go.



## Prerequisites

- Go >= 1.24.0



## Example

Project example can be found [here](https://github.com/distninja/target/blob/main/example/main.go).



## Ninja

```bash
# List ninja subtools
ninja -t list

# List targets by their rule or depth in the DAG
ninja -f /path/to/build.ninja -t targets

# Show inputs/outputs for a path
ninja -f /path/to/build.ninja -t query app
ninja -f /path/to/build.ninja -t targets rule link

ninja -f /path/to/build.ninja -t query main.o
ninja -f /path/to/build.ninja -t targets rule compile_cpp

ninja -f /path/to/build.ninja -t query src/main.cpp

# List all commands required to rebuild given targets
ninja -f /path/to/build.ninja -t commands
ninja -f /path/to/build.ninja -t commands -s app
ninja -f /path/to/build.ninja -t commands -s main.o

# List all inputs required to rebuild given targets (optional)
ninja -f /path/to/build.ninja -t inputs

# List all rules (optional)
ninja -f /path/to/build.ninja -t rules
```



## License

Project License can be found [here](LICENSE).



## Reference

- [ninja](https://github.com/ninja-build/ninja)
