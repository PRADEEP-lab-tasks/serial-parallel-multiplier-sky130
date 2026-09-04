# Serial-Parallel Multiplier on Sky130 (OpenLane Flow)

This repository contains a parameterized Serial-Parallel Multiplier (SPM) implemented in Verilog and synthesized using the **OpenLane flow** targeting the SkyWater SKY130 nm PDK. It demonstrates an end‑to‑end ASIC design flow: from RTL and testbench simulation through synthesis, floorplanning, placement, routing, and signoff.

-----
 This Project Engineer is PRADEEP he knows little about designs so expect little in this project
---

## 📂 Repository Structure

- `src/`  
  Verilog RTL (`sp_multiplier.v`) and constraints (`sp_multiplier.sdc`).

- `tb/`  
  Testbenches for functional verification.

- `openlane/`  
  OpenLane configuration files (`config.json`, `flow.tcl`) and run directories.

- `runs/`  
  Auto‑generated results from OpenLane runs, including synthesis reports, logs, and GDS.

---


### Prerequisites
- Docker installed and configured
- OpenLane environment set up
- SkyWater SKY130 PDK installed

### Simulation
Run functional simulation with Icarus Verilog:
```bash
iverilog -g2012 -o simv src/sp_multiplier.v tb/sp_multiplier_tb.v
vvp simv
gtkwave dump.vcd
