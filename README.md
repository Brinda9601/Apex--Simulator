# APEX Pipeline Simulator v2.0
A template for 5 Stage APEX In-order Pipeline

## Notes:

 - This code is a simple implementation template of a working 5-Stage APEX In-order Pipeline
 - Implementation is in `C` language
 - Stages: Fetch -> Decode -> Execute -> Memory -> Writeback
 - All the stages have latency of one cycle
 - There is a single functional unit in Execute stage which perform all the arithmetic and logic operations
 - Includes logic for `ADD`, `LOAD`, `BZ`, `BNZ`,  `MOVC` and `HALT` instructions
 - On fetching `HALT` instruction, fetch stage stop fetching new instructions
 - When `HALT` instruction is in commit stage, simulation stops

## Files:

 - `Makefile`
 - `file_parser.c` - Functions to parse input file
 - `apex_cpu.h` - Data structures declarations
 - `apex_cpu.c` - Implementation of APEX cpu
 - `apex_macros.h` - Macros used in the implementation
 - `main.c` - Main function which calls APEX CPU interface
 - `input.asm` - Sample input file

## How to compile and run

 Go to terminal, `cd` into project directory and type:
```
 make
```
 Run as follows:
```
 ./apex_sim <input_file_name>
```