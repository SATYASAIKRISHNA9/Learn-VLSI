# Learn-VLSI(PD) With open-source EDA Tools
This respository of 5-day workshop is used to help the beginners to using open-source tools like below to get the base practical idea of the VLSI Physical Design- 


**Yosys** – for Synthesis <br/>
**Graywolf** – for Placement <br/>
**Qrouter** – for Routing <br/>
**Netgen** – for LVS <br/>
**Magic** – for Layout and Floorplanning <br/>
**Qflow** – RTL2GDS integration <br/>
**OpenSTA** & **Opentimer** -Pre-layout and Post-layout Static timing analysis <br/>

# Contents of Workshop 
**Day -1**: Study and Review Various components of RISC-V based PicoSoC <br/>
**Day -2**: Chip Planning Strategies and Introduction to Foundry Library Cells <br/>
**Day -3**: Design and Characterize one Library Cell using magic Layout Tool and ngspice<br/>
**Day -4**: Pre-Layout Timing Analysis and Importance of Good Clock Tree<br/>
**Day -5**: Final Steps for RTL2GDS<br/>

# Day 1 - To get the idea of RISC-V based PicoSoC and its components

The day one responsibilities are to learn about

Introduction to package, chip , pads, die, core, IPs<br/>
Introduction to RISC V<br/>
From software application to hardware<br/>
Pre requesities and RISC V,PICORV32 AND picosoc view<br/>
Raven Soc and full chip review<br/>
Introduction to IC design components and open source EDA tools<br/>
Steps to start synthesizing picorv32, report ratio<br/>
Test open source EDA tools using sample design and VSD flow utility<br/>
Steps to perform labs on platform<br/>


The below image explains about the pads, die, core 

![die, pads, core](https://user-images.githubusercontent.com/79971687/110565346-5825e500-8174-11eb-9822-9bbb336f133c.jpg)

**RISC - V OVERVIEW:**

1.RISC - V available in various flavours i.e genealogy

2.RV32 has 32 bit instructions

Suffixes specify available extensions -I : basic integer instruction set; -M : hardware mulptiplier/divider; -C : compressed instruction set (16 - bit)
PICORV32 OVERVIEW:

key features: 1. Small size 2.High Clock Speed 3.Native Memory Interface 4.Optional IRQ Support

**PICORV32 OVERVIEW:

key features: 1. small size 2.high clock speed 3.native memory interface 4.optional IRQ support

