# Foundations (shared base for VLSI and Embedded)

Everything in this section is needed by both tracks. Do it first.

---

## Level 0 — Absolute beginner

### Electronics basics
- [ ] Voltage, current, resistance, Ohm's law, power
- [ ] Series and parallel circuits, voltage dividers
- [ ] Capacitors, inductors, RC and RL time constants
- [ ] Reading a schematic and a breadboard layout
- [ ] Multimeter and oscilloscope basics

**Resources**
- *The Art of Electronics* — Paul Horowitz & Winfield Hill (book, the standard practical reference)
- Khan Academy: Circuits and Electrical Engineering (video, free)
- Phil's Lab (YouTube) — practical electronics, test equipment, PCB topics (video, free)
- Ben Eater — "Build a breadboard computer" (video, free) — best first hands-on series

### Electromagnetics (EMF) basics
- [ ] Electric and magnetic fields, Coulomb's law, Gauss's law
- [ ] Faraday's law, inductance, transmission lines basics
- [ ] Why traces, grounds, and cables radiate or pick up noise (EMI/EMC)

**Resources**
- *Engineering Electromagnetics* — William Hayt & John Buck (book)
- MIT OpenCourseWare 6.013 Electromagnetics and Applications (video and notes, free)

### Digital electronics
- [ ] Number systems (binary, hex, two's complement)
- [ ] Logic gates, Boolean algebra, Karnaugh maps
- [ ] Combinational logic: adders, multiplexers, decoders
- [ ] Sequential logic: latches, flip-flops, counters, state machines
- [ ] Setup and hold time, clock and metastability basics

**Resources**
- *Digital Design and Computer Architecture* — David Harris & Sarah Harris (book; RISC-V edition available)
- Onur Mutlu — Digital Design and Computer Architecture lectures, ETH Zürich (YouTube, free)
- *Digital Design: Principles and Practices* — John Wakerly (book)
- HDLBits (hdlbits.01xz.net) — interactive Verilog exercises (free)
- Nandland (nandland.com) — beginner FPGA and Verilog tutorials (free)

### Analog electronics
- [ ] Diodes, BJTs, MOSFETs as switches and amplifiers
- [ ] Op-amps, filters, feedback, bias design
- [ ] Noise, gain, bandwidth, and linearity

**Resources**
- *Microelectronic Circuits* — Sedra & Smith (book, standard university text)
- *The Art of Electronics* (see above)

### PCB design basics
- [ ] Component footprints, datasheets, and BOM
- [ ] Schematic capture, layout, layer stackup
- [ ] Routing rules: trace width, clearance, return paths, decoupling caps
- [ ] Gerber files and fabrication (JLCPCB, PCBWay)

**Resources**
- KiCad documentation and KiCad tutorials on YouTube (open-source EDA, free)
- Phil's Lab — PCB design videos (free)
- *Printed Circuit Board Design Techniques for EMC Compliance* — Mark Montrose (book)

### MATLAB / Octave (signal and analysis)
- [ ] Vectors, matrices, plotting
- [ ] FFT, filters, signal visualisation
- [ ] Simulink basics for control and DSP

**Resources**
- MATLAB Onramp (free official course from MathWorks)
- GNU Octave (free, open-source MATLAB-compatible tool)
- *Signals and Systems* — Oppenheim & Willsky (book)

### Linux, Git and scripting
- [ ] Shell commands, file system, permissions
- [ ] Git basics: commit, branch, merge, pull request
- [ ] Python basics for test scripts and automation

**Resources**
- *The Linux Command Line* — William Shotts (book, free PDF from the author)
- *Pro Git* — Scott Chacon & Ben Straub (free online)
- Python.org official tutorial (free)

---

## Level 1 — Foundation

- [ ] Read a datasheet end-to-end and pick a part for a design
- [ ] Learn the difference between sim, emulation and real hardware
- [ ] Build a simple RC filter and measure it on a scope

## Level 2 — Intermediate

- [ ] Design a small analog front end (sensor to ADC)
- [ ] Design a 4-layer PCB with proper power and ground planes
- [ ] Run a basic SPICE simulation of an amplifier

## Level 3 — Advanced

- [ ] Explain setup/hold, metastability, and signal integrity to a peer
- [ ] Do a full schematic-to-Gerber design review of a board you designed

---

## Checkpoint project (Level 0 to 1)

Build a 555-timer or microcontroller-based LED flasher on a breadboard. Then build it again as a PCB in KiCad. Document both in your repo.
