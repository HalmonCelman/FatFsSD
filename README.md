# FatFs SD by SPI library

This repository is **modified** copy of FatFs code by ChaN.

## Assumptions:
- configurable without changing anything in repo files
- easy to run

## How to use this repo ( recommended way )
1. Add as a subdirectory
2. Write or take from somwhere driver file and "add" to your project anywhere: [***How to write driver file***](driver_file.md)
3. Copy `ffconf.h` file into the parent folder(f.e. if you have your ffconf.h at External/FatFsSD then you should copy it into External/)
4. Compile everything, if you are using cmake for this CMakeLists in this repo will create **FatFs** library

## Some Examples?

I will upload some examples as soon as I can.