# FIFO (SystemVerilog)

Simple FIFO example written in SystemVerilog.

Repository structure

- `FIFO.sv` — FIFO module (SystemVerilog).
- `tb.sv` — Testbench for the FIFO (SystemVerilog).

Purpose

This repository provides a compact FIFO implementation and a self-contained testbench to simulate its behavior. It's intended for learning, simple verification tasks, and as a starting point for integration into larger projects.

Quick start — prerequisites

Install one of the following simulators:

- ModelSim / Questa (Mentor/Siemens)
- Synopsys VCS
- Icarus Verilog + Verilog-Perl or other SV extensions (limited SystemVerilog support)

If you don't have a commercial simulator, use Icarus Verilog for basic Verilog tests, but note SystemVerilog features may be unsupported.

Simulate using ModelSim / Questa (recommended for SystemVerilog)

Open PowerShell in this project folder and run:

# Compile

vlog FIFO.sv tb.sv

# Run

vsim -c work.tb -do "run -all; quit"

Simulate using Synopsys VCS

# Compile & elaborate

vcs -sverilog FIFO.sv tb.sv -o simv

# Run

./simv +vcs+vcdpluson

Simulate using Icarus Verilog (limited SV support)

Icarus Verilog has limited SystemVerilog support. For simple behavioral tests (if compatible):

# Compile

iverilog -g2012 -o simv FIFO.sv tb.sv

# Run

Notes

- Adjust compile/run commands for your simulator installation path and licensing requirements.
- If the testbench uses advanced SystemVerilog features, prefer ModelSim/Questa or VCS.

Contact

For questions, open an issue or contact the repository owner.
