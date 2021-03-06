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

**PICORV32 OVERVIEW:**

key features: 1. Small size 2.High Clock Speed 3.Native Memory Interface 4.Optional IRQ Support

**Lab**

Yosys is a command to open the yosys terminal.

![Yosys](https://user-images.githubusercontent.com/79971687/110567365-64f80800-8177-11eb-879a-befa26cd7fbc.jpg)

The command ./vsdflow spi_slave_design_details.csv is to initialize the design & execute like the following image

![Screen Shot 2021-03-04 at 11 08 20 AM](https://user-images.githubusercontent.com/79971687/110568267-bead0200-8178-11eb-91ba-1739c24cfea0.png)


qflow is a command to display the spi_slave layout view

![Screen Shot 2021-03-04 at 11 12 39 AM](https://user-images.githubusercontent.com/79971687/110568586-38dd8680-8179-11eb-908d-62f40d3a1ead.png)

The below is the tkcon window which is used to excute the commands in the layout view. Ex:- box is a command to excute the length, width & area of the layout 

![Screen Shot 2021-03-04 at 11 41 47 AM](https://user-images.githubusercontent.com/79971687/110569015-e94b8a80-8179-11eb-9302-498ada8f19f3.png)

To know the %ratio of flipflop/total logic

When we run the synthesis operation in qflow manager 

![Screen Shot 2021-03-04 at 11 33 54 AM](https://user-images.githubusercontent.com/79971687/110570560-18fb9200-817c-11eb-908e-7e62f8309930.png)

Ratio of flops to logic cells = Total number of flops / Total number of cells from the below image

![logic](https://user-images.githubusercontent.com/79971687/110570658-49433080-817c-11eb-938d-b370e4416666.jpg)

Flops/Total logic = 1613/13197 = 12.22%

# DAY-2 : Chip planning strategies and introduction to Foundry Library Cells

The day two responsibilities are to learn about

Utilization factor and Aspect Ratio
Concept of preplaced cells
De coupling capacitors
Power planning
Pin placement and logical cell placement blockage
Pin arrangement UI and automatic grouping of vectors
Tips on pin placement and floorplanning chip
Floorplanning labs
Netlist binding and initial place design
Optimize placement using estimated wire length and capacitance
Final placement optimization
Need for libraries and characterization
Inputs for cell dessign flow
Circuit design step
Layout design step
Typical characterization flow
Timing threshold definitions
Propogation delay and transition time

**Lab :**

![Screen Shot 2021-03-04 at 11 12 39 AM](https://user-images.githubusercontent.com/79971687/110619361-b9be7180-81bd-11eb-8a8f-0af8cdf4769f.png)

The below figures are the pinplacement procedure that we follow.As the qflow is opened we will synthesis the design and in the placement settings we should click on the arrange pins option and there reset,clk pins must be grouped by newgroup by naming it.After that the iterations of standard cell and pins are taken place.

![Screen Shot 2021-03-04 at 5 19 01 PM](https://user-images.githubusercontent.com/79971687/110620279-d8713800-81be-11eb-9b50-58f2de7c3da9.png)

These are iterations that are happened in the placement stage based on some algorithms and nearest pin specified in the netlist.

![Screen Shot 2021-03-04 at 5 22 23 PM](https://user-images.githubusercontent.com/79971687/110620503-15d5c580-81bf-11eb-8c9a-e8b69b505c85.png)

The below images explains the placement have iterations to make the cells closer to get the best path.

![Screen Shot 2021-03-04 at 5 23 26 PM](https://user-images.githubusercontent.com/79971687/110620657-461d6400-81bf-11eb-9076-be41789858e4.png)

![Screen Shot 2021-03-04 at 6 00 49 PM](https://user-images.githubusercontent.com/79971687/110621028-c5ab3300-81bf-11eb-884f-791627d9cc68.png)

