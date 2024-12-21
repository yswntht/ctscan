# CTScan
**CTScan: A CGRA-based Platform for Emulation of Power Side-Channel Attacks on Edge CPUs**

The following are the items we are making available for public release:

1. **CTScan (Rocket CPU)**  
    1. We are releasing AES S-box protected and unprotected manually written mappings of CTScan.  
    2. We refer you to the HyCUBE open-source RTL, on which we tested the execution of the released mappings.  
    3. Refer to the "Programming HyCUBE" section to run the mappings.  
    4. Our gate-level evaluations in the paper were conducted using commercial CAD tools, commercial PDK, and a commercial SRAM-memory generator. As these are licensed, we cannot release them.  
    5. Refer to the correlation analysis script for the attack description.  

2. **Sakura-X FPGA (Baseline 1)**  
    1. We are releasing the bitstream for the Sakura-X board for Rocket CPU. We are also releasing the software for AES S-box protected and unprotected implementations.  
    2. Refer to the "Programming FPGA" section.  
    3. We use 'Rocket32b' available in the list of default configurations. For different configurations, users are expected to port the Chisel code base onto Sakura-X and modify the Chisel generator configurations themselves.  
    4. For software other than AES S-box, refer to the RISC-V GCC compiler support and follow the "Programming FPGA" section.  
    5. Refer to the correlation analysis script for the attack description.  

3. **SiFive-FE310 (Golden reference)**  
    1. Refer to the LoFive website for the board layout.  
    2. Refer to the "Programming CPU Chip" section to execute the software application.
