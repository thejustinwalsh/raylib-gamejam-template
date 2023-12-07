# raylib-gamejam-template
> Minimalistic template to kickoff your gamejam entry using [raylib](https://www.raylib.com)

- [x] CMake build system for desktop and web with automatic resource copying and bundling
- [x] VSCode configuration and extension recommendations
- [x] Github Actions CI for desktop and web

*To get started, click the green `Use this template` button on the top of the repository page.*

<br/>

## Dependencies

```
brew install emscripten cmake ninja
```

## Build

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

#### Notes

- While iterating on your project setup and adding dependencies or resources sometimes cmake needs a hard reset.  
- Resources that are removed from the `./resources` folder aren't removed from the build folder[^1], this has no effect on the resource bundeling, but you may accumulate resources that are no longer used.  
- To reset your setup, delete your `./build` folder and run `cmake -B ./build` again.
[^1]: Accepting pull requests

## Run

```sh
./build/raylib_gamejam_template
- or -
emrun ./build-web/raylib_gamejam_template.html
```

<br/>
<br/>

*Forked from [raylib-cpp](https://github.com/RobLoach/raylib-cpp) examples by @RobLoach*
