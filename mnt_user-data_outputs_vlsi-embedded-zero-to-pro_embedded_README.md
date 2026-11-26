# Embedded Systems Track

From absolute beginner to a professional embedded engineer: Assembly, C/C++, protocols, hardware, firmware, and STM32.

Start with [`../foundations/`](../foundations/README.md) if you have not done the electronics basics.

---

## Level 0 — Absolute beginner

### Microcontroller basics
- [ ] What a microcontroller is, and how it differs from a CPU
- [ ] GPIO: input, output, pull-up, pull-down
- [ ] Blinking an LED, reading a button
- [ ] Simple debugging with a serial print

**Resources**
- Arduino official tutorials (free, good for first contact)
- Wokwi (wokwi.com) — browser simulator for Arduino, ESP32, STM32, and RP2040 (free)
- *Make: Electronics* — Charles Platt (book, hands-on)
- Shawn Hymel (YouTube) — embedded tutorials (free)

### C basics
- [ ] Variables, types, pointers, arrays, structs, bitwise operations
- [ ] Memory layout: stack, heap, globals, `volatile`
- [ ] Writing a register-level driver

**Resources**
- *The C Programming Language* — Kernighan & Ritchie (book, classic)
- *Beej's Guide to C* (free online)
- *Embedded C Programming and the Atmel AVR* — Richard Barnett (book)

---

## Level 1 — Foundation

### Assembly language

**Why:** Assembly teaches you what the CPU really does. You do not need to write whole programs in it, but you must read it when debugging.

#### x86
- [ ] Registers, flags, addressing modes, stack, calls
- [ ] Writing small routines and linking with C

**Resources**
- *Assembly Language for x86 Processors* — Kip Irvine (book, widely used)
- *Programming from the Ground Up* — Jonathan Bartlett (free online)

#### ARM (Cortex-M and Cortex-A)
- [ ] Thumb-2 instruction set, register banks, exception model
- [ ] Reading compiler output and disassembly
- [ ] Startup code, vector table, linker script

**Resources**
- *The Definitive Guide to ARM Cortex-M3 and Cortex-M4 Processors* — Joseph Yiu (book)
- ARM Developer documentation (free, official reference manuals)
- *Mastering the ARM Cortex-M4* — ARM official learning resources

#### RISC-V (open ISA)
- [ ] RV32I base integer ISA, load/store architecture
- [ ] Writing bare-metal RISC-V code and running it in simulation
- [ ] Understanding the custom extensions model

**Resources**
- *The RISC-V Reader: An Open Architecture Atlas* — Patterson & Waterman (book)
- *Computer Organization and Design: RISC-V Edition* — Patterson & Hennessy (book)
- riscv.org official specifications (free)
- Spike (RISC-V ISA simulator, open source) and `riscv-tests` (open source)

### C and C++

#### C (Level 1 to 2)
- [ ] Pointers in depth, function pointers, bit fields
- [ ] Interrupt service routines and critical sections
- [ ] MISRA C guidelines (know them; used in automotive)

**Resources**
- *Expert C Programming* — Peter van der Linden (book)
- MISRA C guidelines overview (MISRA publications, paid standard; overviews are free)

#### C++ for embedded (Level 2)
- [ ] Classes without heap allocation, templates for zero-cost abstraction
- [ ] Avoiding exceptions and RTTI in firmware
- [ ] RAII for peripheral and resource handling

**Resources**
- *Embedded Programming with Modern C++* — Lucio Di Toro (book)
- *Effective Modern C++* — Scott Meyers (book)
- cppreference.com (free)

### Protocols

| Protocol | What to learn | Resource |
|----------|---------------|----------|
| UART | Baud rate, framing, parity | Learn with a USB-UART adapter and a terminal |
| SPI | Master/slave, CPOL/CPHA, chip select | Sparkfun SPI tutorial (free) |
| I2C | Start/stop, ACK, addressing, pull-ups | Sparkfun I2C tutorial (free) |
| CAN | Arbitration, error frames, bit timing | *Controller Area Network Primer* (Microchip, free PDF) |
| USB | Enumeration, endpoints, classes | USB.org specs and *USB Complete* — Jan Axelson (book) |
| Ethernet / TCP-IP | Frames, IP, TCP, sockets | *TCP/IP Illustrated, Vol. 1* — Stevens (book) |
| Modbus | Master/slave industrial protocol | Modbus.org specifications (free) |
| SWD / JTAG | Debug interfaces | ARM CoreSight documentation (free) |

---

## Level 2 — Intermediate

### Hardware and firmware

- [ ] Clock trees, PLLs, and power domains on an MCU
- [ ] DMA, timers (PWM, input capture), ADC/DAC
- [ ] Bootloaders and firmware update (OTA basics)
- [ ] Low-power modes and sleep management

**Resources**
- *Making Embedded Systems* — Elecia White (book, practical design)
- *Embedded Systems Architecture* — Tammy Noergaard (book)
- *Introduction to Embedded Systems: Cyber-Physical Systems* — Lee & Seshia (free online textbook)

### STM32 (currently trending; learn this in Level 1 or 2)

- [ ] STM32CubeMX for pin and clock configuration
- [ ] HAL vs LL vs bare-register programming
- [ ] Debugging with SWD, ST-Link, and breakpoints
- [ ] Building a project with CMake or PlatformIO

**Resources**
- *Mastering STM32* — Carmine Noviello (book, free sample chapters and code online)
- ST's free "STM32 MOOC" on st.com (free, official)
- STM32CubeIDE and STM32CubeMX (free from ST)
- libopencm3 (open-source low-level library for STM32 and others)
- Controllers Tech (YouTube) — STM32 and embedded tutorials (free)

### RTOS

- [ ] Tasks, scheduling, priorities, mutexes, semaphores, queues
- [ ] Priority inversion and how to avoid it
- [ ] Interrupt latency and real-time constraints

**Resources**
- FreeRTOS official docs and the book *Mastering the FreeRTOS Real Time Kernel* (free PDF from freertos.org)
- Zephyr RTOS documentation (open source, Linux Foundation project)
- *Patterns for Time-Triggered Embedded Systems* — Michael Pont (book)

---

## Level 3 — Advanced / Pro

- [ ] Write a bootloader and a board support package (BSP)
- [ ] Use a debugger and trace tools to find memory corruption and timing bugs
- [ ] Unit test firmware on the host (Unity, CMock)
- [ ] Functional safety basics (IEC 61508, ISO 26262 for automotive)
- [ ] Write a device driver for Linux (kernel modules) on an embedded SoC

**Resources**
- *Test-Driven Development for Embedded C* — James Grenning (book)
- *Real-Time Embedded Components and Systems with Linux and RTOS* — Stuart Cording (book)
- Linux kernel documentation (free)

---

## Open-source tools for embedded

| Tool | Purpose |
|------|---------|
| GNU Arm Embedded Toolchain (gcc-arm-none-eabi) | Compile for ARM Cortex-M |
| RISC-V GNU toolchain | Compile for RISC-V |
| PlatformIO | Build and flash across many boards |
| OpenOCD | On-chip debugging via JTAG/SWD |
| GDB | Debugger |
| QEMU | Emulate boards and CPUs |
| Renode | Full-system embedded simulator (open source) |
| Wokwi | Browser simulator (free tier) |
| CMake | Build system |
| Unity / CMock | Unit testing for C |
| Ghidra | Reverse engineering and disassembly |
| Logic analyser software: PulseView / sigrok | Decode UART, SPI, I2C from a cheap logic analyser |
| Saleae Logic (free software; hardware paid) | Protocol analysis |

---

## Checkpoint projects

- **Level 0:** Blink an LED and read a button on an STM32 Blue Pill or Nucleo board.
- **Level 1:** Write a UART-based command line on an STM32, and read an I2C temperature sensor.
- **Level 2:** Build a sensor node with an RTOS, DMA-based ADC, and low-power sleep.
- **Level 3:** Build a CAN node or a small bootloader with a custom protocol, and document it with unit tests.
