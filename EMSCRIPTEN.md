# Emscripten

## Build

```
mkdir build
cd build
emcmake cmake ..
emmake make
```

## Link

```
emcc -flto -O3 -fno-rtti -fno-exceptions */*.o */*/*.o -o index.html -sUSE_SDL=2 -sUSE_SDL_MIXER=2 -sSDL2_MIXER_FORMATS=[\"mp3\"] -sUSE_MPG123=1 -sUSE_LIBPNG -lidbfs.js -sENVIRONMENT=web --preload-file Exe/ -sEXPORTED_RUNTIME_METHODS=['allocate'] -sINITIAL_HEAP=128mb
```
