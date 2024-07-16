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
emcc -flto -O3 -fno-rtti -fno-exceptions */*.o */*/*.o -o index.html -s USE_SDL=2 -s USE_SDL_MIXER=2 -s SDL2_MIXER_FORMATS=[\"mp3\"] -s USE_MPG123=1 -s USE_LIBPNG -sINITIAL_MEMORY=512mb -sENVIRONMENT=web --preload-file Exe/ --closure 1 -sEXPORTED_RUNTIME_METHODS=['allocate']
```
