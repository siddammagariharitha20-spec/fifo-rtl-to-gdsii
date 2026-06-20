# FIFO Memory Design — RTL to GDSII (ASIC Physical Design)

## Overview
8-bit wide, 8-deep synchronous FIFO designed in Verilog and implemented through complete RTL-to-GDSII physical design flow using OpenLane and SkyWater Sky130 (130nm) open-source PDK.

## Tools Used
- RTL Design: Verilog
- Synthesis: Yosys
- Physical Design: OpenLane / OpenROAD
- PDK: SkyWater Sky130A
- Layout Viewer: KLayout

## Design Details
- Module: 8-bit data width, 8-deep FIFO
- Ports: clk, rst, wr_en, rd_en, data_in[7:0], data_out[7:0], full, empty

## Results

| Clock Frequency | Period | Timing Slack | Status |
|-----------------|--------|---------------|--------|
| 50 MHz | 20 ns | 15.93 ns | MET |
| ~143 MHz | 7 ns | 3.26 ns | MET |

- Cell Count: 345 standard cells
- Chip Area: 3951.29 um^2
- DRC Violations: 0
- Setup/Hold Violations: 0 (at both frequencies)

## Files
- fifo.v — RTL source code
- fifo.gds — Final GDSII layout (50MHz run)
- final_150mhz.gds — Final GDSII layout (150MHz run)
- 1-synthesis.AREA_0.stat.rpt — Synthesis cell/area report
- 3-initial_fp_die_area.rpt — Floorplan die area report
