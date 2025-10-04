# Simulation and analysis of VSDBabySoC
-----------

### 1. Clone the VSDBabySoC project repo
```bash
   $ git clone https://github.com/manili/VSDBabySoC.git
   $ cd VSDBabySoc
   $ mkdir -p output/pre_synth_sim                   // store presynthesis simulation results
```
### 2. Convert tlv to verilog 

```bash
   $ pip install pyyaml click sandpiper-saas       // these packages are required to convert tlv to verilog
   $ show pyyaml click sandpiper-saas             // check whether these packages are successfully installed or not
```
<p align="center">
  <img src="assets/python_packages.png" alt="yosys" height="500" width="800"/>
</p>

```bash
   $ sandpiper-saas -i ./src/module/*.tlv -o rvmyth.v --bestsv --noline -p verilog --outdir ./src/module
```
<p align="center">
  <img src="assets/tlv_to_v_2.png" alt="yosys" height="500" width="800"/>
</p>
Now tlv (transaction level verilog) to verilog conversion of rvmyth (RISC-V core) is successful.

### 3. Pre Sythesis Simulation
```bash
   $ iverilog -o output/pre_synth_sim/pre_synth_sim.out -DPRE_SYNTH_SIM \
    -I src/include -I src/module \
    src/module/testbench.v src/module/vsdbabysoc.v
   $ cd output/pre_synth_sim
   $ ./pre_synth_sim.out
   $ gtkwave pre_synth_sim.vcd
```
<p align="center">
  <img src="assets/pre_synth_output_wave.png" alt="yosys" height="500" width="800"/>
</p>

