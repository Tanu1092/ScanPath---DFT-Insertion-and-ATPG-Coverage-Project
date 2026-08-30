# DFT Project – Scan Path & ATPG Demonstration
GitHub Live Repository: https://github.com/Tanu1092/ScanPath---DFT-Insertion-and-ATPG-Coverage-Project

This folder contains a simple educational DFT source-code project using Verilog.

## Files
- `scan_dff.v` – Scan-enabled D flip-flop.
- `scan_chain.v` – 4-bit serial scan chain.
- `alu_8bit.v` – 8-bit ALU functional block.
- `dft_alu_top.v` – Top-level DFT-enabled ALU.
- `dft_alu_tb.v` – Testbench for functional and scan operation.

## Simulation with Icarus Verilog

Install Icarus Verilog and run:

```text
iverilog -o dft_sim scan_dff.v scan_chain.v alu_8bit.v dft_alu_top.v dft_alu_tb.v
vvp dft_sim
```

A waveform file `dft_alu_tb.vcd` is generated. It can be viewed with GTKWave:

```text
gtkwave dft_alu_tb.vcd
```

## Project flow
1. Design the functional circuit.
2. Add scan-enabled flip-flops.
3. Connect flip-flops into a scan chain.
4. Verify scan shift operation.
5. Run functional simulation.
6. Apply test patterns for DFT/ATPG demonstration.
7. Analyze waveform and fault-detection behavior.

This is an educational RTL-level DFT demonstration, not a production ASIC DFT insertion flow.
