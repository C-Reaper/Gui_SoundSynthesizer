# Project README

## Overview
The project is a simple sound board application that can be built and run on Linux, Windows, Wine, or WebAssembly. It uses a custom library for graphics rendering and a sound library for audio playback.

## Features
- Sound Board Interface
- Play sounds by pressing buttons
- Display button state (on/off)

## Project Structure

### Prerequisites
- C/C++ Compiler and Debugger (GCC, Clang)
- Make utility
- Standard development tools
- Libraries needed in specific projects:
  - X11 for graphics on Linux
  - ALSA for audio playback on Linux
  - Wine API for Windows compatibility
  - SDL2 for WebAssembly

## Build & Run
### Building on Linux
To build the project on Linux, use one of the following commands:
```sh
make -f Makefile.linux all      # build output
make -f Makefile.linux do       # build + exe output
make -f Makefile.linux clean    # Remove build artifacts
```

### Running on Linux
After building, you can run the application using:
```sh
make -f Makefile.linux exe
```

### Building on Windows
To build the project on Windows, use one of the following commands:
```sh
make -f Makefile.windows all      # build output
make -f Makefile.windows do       # build + exe output
make -f Makefile.windows clean    # Remove build artifacts
```

### Running on Windows
After building, you can run the application using:
```sh
make -f Makefile.windows exe
```

### Building for Wine
To build the project for use with Wine, use one of the following commands:
```sh
make -f Makefile.wine all      # build output
make -f Makefile.wine do       # build + exe output
make -f Makefile.wine clean    # Remove build artifacts
```

### Running on Wine
After building, you can run the application using:
```sh
make -f Makefile.wine exe
WINEPREFIX=~/wine64 WINEARCH=win64 wine $(TARGET)
```

### Building for WebAssembly
To build the project for use in a web browser, use one of the following commands:
```sh
make -f Makefile.web all      # build output
make -f Makefile.web do       # build + exe output
make -f Makefile.web clean    # Remove build artifacts
```

### Running on WebAssembly
After building, you can run the application by opening the generated `index.html` file in a web browser.