# CTScan
**CTScan: A CGRA-based Platform for Emulation of Power Side-Channel Attacks on Edge CPUs**

**Overview**



<img width="578" alt="image" src="https://github.com/user-attachments/assets/d4e1661b-141e-4af5-bb20-ea502e36bfa5" />


# **Release information (landing soon!!!)**

The following are the items we are making available for public release:

1. **CTScan (Rocket CPU)**  
    1. [🔜] We are releasing AES S-box protected and unprotected manually written mappings of CTScan.  
    2. [🔜] We refer you to the HyCUBE [open-source RTL](https://github.com/ecolab-nus/HyCUBE), on which we tested the execution of the released mappings.  
    3. [🔜] Refer to the "Programming HyCUBE" section to run the mappings.  
    4. Our gate-level evaluations in the paper were conducted using commercial CAD tools, commercial PDK, and a commercial SRAM-memory generator. As these are licensed, we cannot release them. However, you may refer to open-source counterparts for these tools like [FreePDK](https://github.com/mflowgen/freepdk-45nm), [OpenRAM](https://dl.acm.org/doi/10.1145/2966986.2980098) etc.   
    5. [🔜] Refer to the correlation analysis script for the attack description.
    6. To generate mappings of your own we suggest following method:
        1. Refer to the walk-through example from the paper.
        2. To assist you in translating the mapping from CGRA assembly program to CGRA binary, you may use our python scripts. These scripts produce final data-memory and configuration-memory files.
        3. HyCUBE instruction format for compute and network configurations is defined in [HyCUBE-DAC](https://ieeexplore.ieee.org/document/8060417) [HyCUBE-A-SSCC](https://ieeexplore.ieee.org/abstract/document/9056954).
        4. We also suggest you to check the functional correctness of the user-generated mappings on [hycube c++ simulator](https://github.com/ecolab-nus/morpher) first below attempting VCD based verification and debugging using simulation tools like verilator. 
                

2. **Sakura-X FPGA (Baseline)**  
    1. [✔️] We are releasing the bitstream for the Sakura-X board for Rocket CPU. We are also releasing the software for AES S-box protected and unprotected implementations.  
    2. [🔜] Refer to the "Programming FPGA" section.  
    3. We use 'Rocket32b' available in the list of default configurations. For different configurations, users are expected to port the Chisel code base onto thier side-channel FPGA platform (e.g. Sakura-X or Chipwhisperer) and modify the [Chisel generator configurations](https://github.com/eugene-tarassov/vivado-risc-v) themselves.  
    4. [🔜] For software other than AES S-box, refer to the RISC-V GCC compiler support and follow the "Programming FPGA" section.  
    5. [🔜] Refer to the correlation analysis script for the attack description.  

3. **SiFive-FE310 (Golden reference)**  
    1. [🔜] Refer to the [Lofive website](https://github.com/mwelling/lofive) for details of software toolchain setup, and various other dependencies to get started on 'hello world' program. In our evaluations, we use Lofive-R1 board with SiFive Freedom E310 microcontroller.  
    2. [🔜] Refer to the "Programming CPU Chip" section to execute the software application.
  
```bibtex
@article{10.1145/3721294,
author = {Tavva, Yaswanth and Juneja, Rohan and Carlson, Trevor E. and Peh, Li-Shiuan},
title = {CTScan: A CGRA-based Platform for the Emulation of Power Side-Channel Attacks on Edge CPUs},
year = {2025},
publisher = {Association for Computing Machinery},
address = {New York, NY, USA},
issn = {1936-7406},
url = {https://doi.org/10.1145/3721294},
doi = {10.1145/3721294},
journal = {ACM Trans. Reconfigurable Technol. Syst.}
}
