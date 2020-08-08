# lcov

CMake module provides `lcov` based coverage calculation target

## Usage

Assuming your tests are in the `$PROJECT_SOURCE_DIR/tests` directory. Add
`coverage.cmake` into project subdirectory `cmake` and put this lines into
your CMakeLists.txt:

```cmake
set(CMAKE_MODULE_PATH "${CMAKE_MODULE_PATH};${PROJECT_SOURCE_DIR}/cmake")

option(RUN_TESTS "Enable tests" OFF)

include(coverage)

if (RUN_TESTS)
    enable_testing()
    add_coverage_target("*/tests/*")
    add_subdirectory(tests)
endif()
```

## License 

See the [LICENSE](https://raw.githubusercontent.com/cmake-modules/lcov/master/LICENSE) file.
