# IS1200 Computer Hardware Engineering Mini Project

This repository contains my final mini project for the IS1200 Computer Hardware Engineering course, focusing on low-level programming and hardware-software integration.

## Snail Run
**Snail Run** is a real-time endless runner game built for the DE10-Lite FPGA board, which utilizes the RISC-V instruction set. The game challenges players to survive by switching between three fixed lanes to avoid oncoming obstacles, with the difficulty scaling up over time as obstacles spawn and move faster. 

### Key Technical Features
* **Languages:** Implemented primarily in C, utilizing snippets of Assembly specifically for interrupt handling.
* **Hardware Integration:** Renders live game graphics to a VGA display, handles responsive input via on-board switches and keys, and outputs the live score to the board's 7-segment displays.
* **Performance Analysis:** Conducted a deep-dive hardware performance analysis using DTEK-V hardware performance counters via inline assembly. The analysis tracked clock cycles, instruction cache hit rates, and data hazards to compare unoptimized and optimized compiler versions.

### Documentation
Please refer to the included PDF reports for a full breakdown of the game logic and hardware profiling:
* **[Extended Abstract (PDF)](Extended%20Abstract_SnailRun.pdf):** Details the game loop, state updates, graphics rendering, and testing methodology.
* **[Performance Analysis (PDF)](Performance_Analysis___Snail_Run.pdf):** Details the processor architecture analysis, cache limitations, and IPC measurements.

### Acknowledgments
This project was developed collaboratively with **Astrid Leonard**. 
