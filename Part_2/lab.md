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
  <img src="assets/python_packages.png" alt="yosys" height="400" width="800"/>
</p>

```bash
   $ sandpiper-saas -i ./src/module/*.tlv -o rvmyth.v --bestsv --noline -p verilog --outdir ./src/module
```

