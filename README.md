# IS1200 Computer Hardware Engineering Mini Project

This repository contains my final mini project for the IS1200 Computer Hardware Engineering course, focusing on low-level programming and hardware-software integration.

## Snail Run
**Snail Run** is a real-time endless runner game built for the DE10-Lite FPGA board, which utilizes the RISC-V instruction set. The game challenges players to survive by switching between three fixed lanes to avoid oncoming obstacles, with the difficulty scaling up over time as obstacles spawn and move faster. 

### Repository Structure
```text
Snail-Run-IS1200-Hardware-Project/
├── assets/                  # Game graphics and visual assets
├── docs/                    # Technical reports and performance analysis
│   ├── Extended-Abstract-SnailRun.pdf
│   └── Performance-Analysis-Snail-Run.pdf
├── src/                     # Source code (C and Assembly)
│   ├── boot.S
│   ├── dtekv-lib.c
│   ├── dtekv-lib.h
│   ├── dtekv-script.lds
│   ├── main.c
│   └── softfloat.a
├── Makefile                 # Compilation script
└── README.md                # Project documentation
```

### Key Technical Features
* **Languages:** Implemented primarily in C, utilizing snippets of Assembly specifically for interrupt handling.
* **Hardware Integration:** Renders live game graphics to a VGA display, handles responsive input via on-board switches and keys, and outputs the live score to the board's 7-segment displays.
* **Performance Analysis:** Conducted a deep-dive hardware performance analysis using DTEK-V hardware performance counters via inline assembly. The analysis tracked clock cycles, instruction cache hit rates, and data hazards to compare unoptimized and optimized compiler versions.

### How to Compile and Run
To compile and run this project on the DE10-Lite (DTEK-V) board, follow these steps:

1. Extract all files into a local directory.
2. Open your terminal and navigate to the directory containing the files.
3. Compile the project using the `make` command:
   ```bash
   make
   ```
4. Run the compiled binary on the board:
   ```bash
   dtekv-run main.bin
   ```

### Inputs and Outputs
* **Display:** Renders graphics to a connected VGA display.
* **Score:** Outputs the live score to the board's 7-segment displays.
* **SW0:** Flick to move the snail upwards.
* **SW1:** Flick to move the snail downwards.
* **KEY1:** Press to reset the game when a "GAME OVER" is reached.
* **KEY0:** Press to reset the board.

### Documentation
Please refer to the included PDF reports for a full breakdown of the game logic and hardware profiling:
* **[Extended Abstract (PDF)](docs/Extended-Abstract-SnailRun.pdf):** Details the game loop, state updates, graphics rendering, and testing methodology.
* **[Performance Analysis (PDF)](docs/Performance-Analysis-Snail-Run.pdf):** Details the processor architecture analysis, cache limitations, and IPC measurements.

### Acknowledgments
This project was developed collaboratively by:
* **Alex Ryström** 
* **Astrid Leonard** 
