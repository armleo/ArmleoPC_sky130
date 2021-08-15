# ArmleoPC_sky130
ArmleoPC_sky130 is a System-on-Chip integrating ArmleoCPU dual-core RV32IMA CPU capable of booting Linux taped out using Skywater 130nm Technology and open source standard cell library. See: https://github.com/armleo/ArmleoPC_sky130  
Currently this repository is empty but in the future will contain Caravel/Caravan based auto-build project using GitHub CI.  

Block diagram  
<img src="docs/Block diagram.png" alt="ArmleoPC structure" width="400"/>

# ArmleoCPU
ArmleoCPU is RISC-V CPU with Atomics, Multiplier/divider, Cache, MMU, TLB, and will be capable of booting Linux. Two small area cores will be implemented, providing 0.6 IPC @ ~50-75MHz, mainly limited by I/O.

GitHub where everything happens: https://github.com/armleo/ArmleoCPU

# SoC
System includes JTAG for debugging, timers, UARTs, SPIs and GPIO alongside a memory controller.

Memory controller implements PSRAM/Flash controller with combined FPGA connection interface.

If enough time is left then IQ Modulator/Demodulator with external PLL will be designed.

# Limitations
The main limitation for this project is GPIO speed which is limited to 33MHz and the lack of GPIO pins (only ~38). If possible custom GPIO cells will be implemented with a target VDDIO of 1.8V or 3V3 depending on which we can achieve reasonable speeds.

# Links
You can see top level repository with all the links and short descriptions here: https://github.com/armleo/ArmleoPC
