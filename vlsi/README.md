# VLSI Track (Chip Design)

From absolute beginner to a professional VLSI engineer: digital and analog design, frontend and backend flows, verification, DFT, timing, mixed-signal, PDKs, and open-source tools.

Start with [`../foundations/`](../foundations/README.md) first.

---

## Level 0 — Absolute beginner

### What is VLSI?
- [ ] How a transistor works (MOSFET as a switch)
- [ ] CMOS inverter, NAND, NOR
- [ ] The chip design flow from specification to tape-out
- [ ] Moore's law and why process nodes matter

**Resources**
- *Digital Integrated Circuits: A Design Perspective* — Rabaey, Chandrakasan & Nikolić (book)
- Nand2Tetris — "The Elements of Computing Systems" (free course at nand2tetris.org, builds a computer from NAND gates)
- Matt Venn — "Zero to ASIC" course and YouTube videos (free, open-source chip design)
- Ben Eater's breadboard computer series (free)

### Your first simulation
- [ ] Install Icarus Verilog and GTKWave
- [ ] Write a simple Verilog module and a testbench
- [ ] View waveforms

**Resources**
- Icarus Verilog (open source simulator)
- GTKWave (open source waveform viewer)
- HDLBits (free exercises)

---

## Level 1 — Foundation

### Digital design (RTL)
- [ ] Verilog basics: wire, reg, always, assign, blocking vs non-blocking
- [ ] Design a counter, a FIFO, and a UART transmitter in RTL
- [ ] Coding style for synthesis (synthesisable vs not)
- [ ] SystemVerilog basics: `logic`, `always_ff`, `always_comb`, interfaces

**Resources**
- *Digital Design and Computer Architecture* — Harris & Harris (book)
- *SystemVerilog for Verification* — Chris Spear & Greg Tumbush (book)
- *FPGA Prototyping by SystemVerilog Examples* — Pong Chu (book)
- Verible (open-source SystemVerilog linter and formatter)
- Yosys (open-source synthesis tool)

### Synthesis and FPGA
- [ ] Synthesise RTL to gates and see the netlist
- [ ] Targeting FPGA with open tools (Yosys + nextpnr)

**Resources**
- Yosys and nextpnr (open source)
- Project IceStorm and iCE40 boards (open source FPGA toolchain)

### Computer architecture basics
- [ ] Pipelines, hazards, caches, and memory hierarchy
- [ ] RISC-V pipeline design as a practice project

**Resources**
- *Computer Architecture: A Quantitative Approach* — Hennessy & Patterson (book)
- Onur Mutlu lectures on computer architecture, ETH Zürich (YouTube, free)

---

## Level 2 — Intermediate

### Frontend design (RTL to netlist)
- [ ] RTL design and coding guidelines
- [ ] Lint and CDC (clock domain crossing) checks
- [ ] Logic synthesis constraints (SDC)
- [ ] Equivalence checking basics

**Resources**
- Yosys (synthesis, open source)
- Verilator (fast open-source simulator and lint tool)
- *Principles of CMOS VLSI Design* — Weste & Harris (book)

### Backend design (netlist to GDSII)
- [ ] Floorplanning, power planning, placement
- [ ] Clock tree synthesis (CTS)
- [ ] Routing, DRC, LVS
- [ ] Parasitic extraction

**Resources**
- *Principles of CMOS VLSI Design* — Weste & Harris (book)
- *CMOS VLSI Design: A Circuits and Systems Perspective* — Weste & Harris (book, updated edition)
- OpenROAD (open-source RTL-to-GDSII flow)
- OpenLane (open-source flow, built on OpenROAD)
- Magic VLSI (open-source layout editor)
- KLayout (open-source layout viewer and editor)
- Netgen (open-source LVS tool)

### Analog and mixed-signal basics
- [ ] MOSFET small-signal models, current mirrors, differential pairs
- [ ] Op-amp design, bandgap references, LDOs
- [ ] Data converters (ADC/DAC) basics

**Resources**
- *Design of Analog CMOS Integrated Circuits* — Behzad Razavi (book, the standard analog IC text)
- *Microelectronic Circuits* — Sedra & Smith (book)
- *CMOS Analog Circuit Design* — Phillip Allen & Douglas Holberg (book)
- Ngspice (open-source SPICE simulator)
- Xschem (open-source schematic editor)

### Static timing analysis (STA)
- [ ] Setup and hold analysis
- [ ] Clock skew, OCV, multi-corner analysis
- [ ] Writing and reading SDC constraints

**Resources**
- *Static Timing Analysis for Nanometer Designs* — Bhasker & Chadha (book)
- OpenSTA (open-source STA engine, also inside OpenROAD)

---

## Level 3 — Advanced / Pro

### Functional verification
- [ ] Testbench architecture and coverage-driven verification
- [ ] SystemVerilog assertions (SVA)
- [ ] UVM (Universal Verification Methodology)
- [ ] Constrained random verification and scoreboards

**Resources**
- *Writing Testbenches using SystemVerilog* — Janick Bergeron (book)
- *A Practical Guide to Adopting the UVM* — Accellera's UVM resources (free)
- Verification Academy by Siemens EDA (free courses)
- cocotb (open-source Python-based verification framework)
- Verilator (open source)

### Design for Testability (DFT)
- [ ] Scan chains, ATPG (automatic test pattern generation)
- [ ] Stuck-at and transition fault models
- [ ] Built-in self-test (BIST), JTAG boundary scan (IEEE 1149.1)

**Resources**
- *Essentials of Electronic Testing for Digital, Memory, and Mixed-Signal VLSI Circuits* — Bushnell & Agrawal (book)
- IEEE 1149.1 JTAG standard (paid, but overviews are free)
- Yosys scan-insertion examples (open source)

### Protocols for SoC design
- [ ] AMBA AXI, AHB, APB (ARM official specifications, free after registration)
- [ ] PCIe basics and PHY interfaces
- [ ] DDR memory interfaces and controllers
- [ ] I2C, SPI, UART, and their verification models

**Resources**
- ARM AMBA specifications (free after registration on developer.arm.com)
- PCI-SIG overviews (free)
- *Computer Organization and Design* — Patterson & Hennessy (book)

### PDKs (Process Design Kits)
- [ ] What a PDK contains: device models, layers, DRC/LVS rules, standard cells
- [ ] Standard cell libraries and IO libraries
- [ ] Working with an open PDK end to end

**Open PDKs**
- SkyWater SKY130 PDK (open, 130 nm, used in Efabless and Tiny Tapeout shuttles)
- GlobalFoundries GF180MCU PDK (open, 180 nm)
- IHP open PDK (open, SG13G2 technology)
- ASAP7 (academic 7 nm predictive PDK, free for research)

**Resources**
- SkyWater PDK documentation (open source on GitHub)
- Efabless open-source chip platform documentation

### Open tools for VLSI (full list)

| Stage | Tool |
|-------|------|
| Simulation | Icarus Verilog, Verilator, cocotb |
| Waveforms | GTKWave, Surfer |
| Synthesis | Yosys |
| Place and route | OpenROAD, OpenLane |
| STA | OpenSTA |
| Layout | Magic, KLayout |
| LVS and DRC | Netgen, Magic, KLayout |
| Analog simulation | Ngspice, Xyce |
| Schematic | Xschem |
| Lint | Verible, Verilator |

### Mixed-signal verification
- [ ] Real number modelling in SystemVerilog and Verilog-A
- [ ] Co-simulation of analog and digital blocks

**Resources**
- *Analog and Mixed-Signal Verification* — relevant chapters in *SystemVerilog for Verification* (book)
- Ngspice with Verilog-A (open source)

---

## Projects

- **Level 0:** Build a NAND-based adder and an ALU in Verilog. Simulate it with Icarus and view waves in GTKWave.
- **Level 1:** Design a UART transmitter and receiver in RTL, with a testbench in cocotb.
- **Level 2:** Take a small RTL block through Yosys synthesis and OpenROAD place and route to GDSII.
- **Level 3:** Submit a design to a shared shuttle such as Tiny Tapeout or Efabless open shuttles, and write up the verification and timing results.

---

## Learning order at a glance

Digital logic → Verilog/RTL → Simulation → Synthesis → STA → Backend (P&R) → Verification (UVM) → DFT → PDK and tape-out.

Analog and mixed-signal can be learned in parallel once you finish the digital foundations.
