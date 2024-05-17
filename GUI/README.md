# GUI

## CMake SDL2 building
```bat
cmake -S . -B build -G "MinGW Makefiles" -DCMAKE_BUILD_TYPE=Release -DSDL_SHARED=OFF -DSDL_TEST=OFF
cmake --build build
```
