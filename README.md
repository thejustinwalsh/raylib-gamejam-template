# raylib-gamejam-template

Use this template to build a [raylib-cpp](https://github.com/RobLoach/raylib-cpp) project using [CMake](https://cmake.org).

## Dependencies

```
brew install emscripten cmake ninja
```

## Build

To build this project, make sure to have CMake installed locally.

### Desktop

```
mkdir build
cmake -B ./build
cmake --build ./build
```

### Web

```
mkdir build
emcmake cmake -B ./build-web -DPLATFORM=Web -DCMAKE_BUILD_TYPE=Release
cmake --build ./build-web
```

## Run

```sh
./build/raylib_gamejam_template
- or -
emrun ./build-web/raylib_gamejam_template.html
```
