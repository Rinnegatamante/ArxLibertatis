Broken unfinished port of ArxLibertatis to the PSVita.

Needs vitagl built with `HAVE_HIGH_FFP_TEXUNITS=1` flag and unpublished (yet) boost port.

Compile with
```bash
mkdir build && cd build
cmake .. -DBUILD_TOOLS=OFF -DBUILD_IO_LIBRARY=OFF -DBUILD_CRASHHANDLER=OFF -DBUILD_CRASHREPORTER=OFF -DUNITY_BUILD=OFF -DCMAKE_BUILD_TYPE=Debug -DDEBUG=ON -DUSE_STATIC_LIBS=ON -DUSE_X11=OFF -DICON_TYPE=none -DUSE_OPENAL=OFF -DCMAKE_TOOLCHAIN_FILE=$VITASDK/share/vita.toolchain.cmake -DSDL2_INCLUDE_DIR=$VITASDK/arm-vita-eabi/include/sdl2/
make -j16
```

Enabling openal causes unintelligible crash. Also, rendering dynamic objects (entities) doesn't work. Other than that, it's perfect lmao

Also,
```
Arx Libertatis is based on the publicly released Arx Fatalis source code. The source code is available under the GPLv3+ license with some additional terms - see the COPYING and LICENSE files for details.
```
