This is the source code for the Better Majora's Mask hack (https://www.romhacking.net/hacks/5122/) by Maroc. This project is based off the 1.12 version of the MM-Randomizer (https://github.com/ZoeyZolotova/mm-rando)

NB: if you wish to build the hack with the dpad icon for masks and ocarina on the right rather than the left, just rename the `build` directory into `build - dpadleft` and rename the `build - dpadright` directory into `build` before running the build script.

Instructions:

- Download the armips assembler: <https://github.com/Kingcom/armips>, build it or download the precompiled version, and put the executable in the `tools` directory, or somewhere in your PATH
- Download the armips assembler: <https://github.com/Alcaro/Flips>, build it or download the binary, and put the executable in the `tools` directory, or somewhere in your PATH
- Put the ROM you want to patch at `roms/base.z64`. This needs to be an uncompressed ROM;
- Run `python scripts/build.py`, which will create the ROM into the `/Output_ROM` directory

To recompile the C modules, use the `--compile-c` option. This requires the N64 development tools to be installed: <https://github.com/glankk/n64>

To generate symbols for the Project 64 debugger, use the `--pj64sym` option:

    python build.py --pj64sym 'path_to_pj64/Saves/THE LEGEND OF ZELDA.sym'
