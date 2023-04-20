# Content

## Prerequisites

In order to build / pack the content in this repo, either
* use native Linux / WSL on Windows
* or install [MSYS2 MinGW64](https://www.msys2.org/) on Windows

When doing the latter, ensure the necessary `make` and `zip` tools are installed by using
```sh
pacman -S zip make
```

Regardless of operating system, you **must** have a pre-built `c4group`(`.exe`) program on your computer.

Such can be obtained by e.g. downloading a release from https://github.com/legacyclonk/LegacyClonk/releases or building it from source at https://github.com/SteamClonk/SteamClonk

## Usage

The `Makefile` in this project describes the build process. To execute it, invoke it like

```sh
make -j16 C4GROUP=/c/Users/Max/Desktop/SteamClonk/build/Debug/c4group.exe
```
where `16` is the number of CPU threads in your system and `/c/Users/Max/Desktop/SteamClonk/build/Debug/c4group.exe` has to be replaced by **the absolute** path  to your obtained `c4group` program.

**Note:** On some systems, instability of the packing process has been observer

If successful, it should create a folder `packed` with all the packed files in it.