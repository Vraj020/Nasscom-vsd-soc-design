# NASSCOMM-VSD-Digital VLSI SoC design and planning(23 APR-6 MAY'25)

Welcome to my documentation for the VSD-IAT workshop! This repository contains my daily learnings, notes, and hands-on work throughout the course.

This workshop focuses on Open-Source ASIC Physical Design Flow, using tools like OpenLane, Magic VLSI, and the Sky130 PDK, allowing students and professionals to gain industry-ready skills in chip design using free and open-source tools.This program, led by industry expert Kunal Ghosh, provides hands-on experience in standard cell design, physical design, and GDSII generation.


## 📖 Table of contents

## 🟢 Day 1: Introduction & Synthesis

- Familiarization with OpenLane / Sky130  
- Physical Design (PnR) stages  
- Design Preparation stage  
- Execution & analysis of Synthesis  


## 🟢 Day 2: Floorplanning & Placement

- Introduction to floorplan phase  
- LEF vs DEF  
- Special cells  
- Execution & analysis of Placement  


## 🟢 Day 3: Standard Cell Design & Characterization

- Std. cell design using Sky130 PDK  
- SPICE simulation in Ngspice  
- Std. cell Characterization  


## 🟢 Day 4: Timing Analysis & Clock Tree Synthesis (CTS)

- PnR with custom cell  
- Clock Tree Synthesis  
- Static Timing Analysis  
- Timing ECOs  


## 🟢 Day 5: RTL-to-GDS Flow Completion

- Routing  
- Algorithm behind TritonRoute  
- SPEF analysis and extraction  

## DAY 1
INTRODUCTION

 On Day 1, we began our journey into the VSD-IAT open-source   physical design flow using OpenLane and the Sky130 PDK. The focus was on understanding the overall flow of ASIC physical design and how synthesis fits into the process.

📘 Topics Covered:

- Overview of the ASIC Physical Design flow
- Introduction to **OpenLane** and **Sky130 PDK**
- Familiarization with the **PnR (Place and Route)** stages
- Understanding the **Design Preparation** stage
- Execution and analysis of the **Synthesis** stage
🔧 Activities Performed:

1. **Explored OpenLane Directory Structure**  
   - Understood where designs, configurations, logs, and results are stored

2. **Initialized a Design with OpenLane**  
   - Set up basic configurations for a sample design (e.g., `picorv32a` or custom RTL)

## Screenshots
![Screenshot (165)](https://github.com/user-attachments/assets/3f9c3893-23a6-4816-a63f-7cf9f9951fd0)
![Screenshot (166)](https://github.com/user-attachments/assets/5f879a9d-eb5c-4f91-8f59-6a6d1d4fe56a)
![Screenshot (169)](https://github.com/user-attachments/assets/37b1a835-7283-4aac-848a-422f4589dfac)
![Screenshot (170)](https://github.com/user-attachments/assets/be83b202-d644-4d60-bac7-5b27cabd6cf9)
![Screenshot (174)](https://github.com/user-attachments/assets/000342b5-4b87-46a0-a40d-90e58386ebd4)
![Screenshot (179)](https://github.com/user-attachments/assets/715072fe-b2fc-4ad5-a851-a9fb4a8b6227)
![Screenshot (180)](https://github.com/user-attachments/assets/a370dade-b40d-45d6-8d86-8b457b5a6ee4)

## Lab- Screenshots
![VirtualBox_vsdworkshop_25_04_2025_16_27_44](https://github.com/user-attachments/assets/810a5b5b-a325-482b-ac98-c558e8cff058)
![VirtualBox_vsdworkshop_25_04_2025_16_31_06](https://github.com/user-attachments/assets/d070f21e-829d-4490-ad71-5211c336f46e)

## Lab 1 - Task
1)Run 'picorv32a' design synthesis using openLANE flow and generate necessary outputs.

2) Calculate the flop ratio
 = no.of d flipflops/total number of cells
 
 Percentage of DFF'S=Flop Ratio*100

 ## Result

 Calculating  the flop ratio
 = no.of d flipflops(1613)/total number of cells(14876)

 0.1084
 
 Percentage of DFF'S=Flop Ratio*100
 
 10.84
![VirtualBox_vsdworkshop_25_04_2025_16_33_35](https://github.com/user-attachments/assets/f7a3beff-5711-4080-a83d-00e4237ea32a)

## DAY 2
 Floorplanning & Placement


📘 Topics Covered:

- Overview of the ASIC Physical Design flow
- Introduction to **OpenLane** and **Sky130 PDK**
- Familiarization with the **PnR (Place and Route)** stages
- Understanding the **Design Preparation** stage
- Execution and analysis of the **Synthesis** stage
🔧 Activities Performed:

1. **Learned About Floorplanning Concepts**  
   - Core utilization, aspect ratio, die/core area definitions
   - Setting up IO pins, macros, and power planning during floorplanning

2. **Studied LEF and DEF Formats**  
   - **LEF**: Contains abstract view of cells (size, pins, blockage info)
   - **DEF**: Describes the actual physical placement of cells in a design

3. **Special Cells Placement**  
   - Added Tap cells for well-tap connections
   - Added Filler cells to fill gaps after placement
   - Added Decap cells for capacitance balancing

4. **Ran Placement Step in OpenLane**  
   - Global Placement followed by Detailed Placement
   - Analyzed timing reports post-placement

## Screenshots
![Screenshot (183)](https://github.com/user-attachments/assets/697e5b36-2737-4379-be89-3a2e3aa26237)
![Screenshot (185)](https://github.com/user-attachments/assets/5aed57d5-a3f3-454c-adc0-3cf9e6c72415)
![Screenshot (186)](https://github.com/user-attachments/assets/f5096160-7e53-4b85-ba00-17e32efbb85e)
![Screenshot (187)](https://github.com/user-attachments/assets/ee38121a-6f4b-4276-b277-ddc833e4d181)
![Screenshot (188)](https://github.com/user-attachments/assets/e1edf6bf-be38-409c-8f22-8627a6ecea5f)
![Screenshot (189)](https://github.com/user-attachments/assets/ee014104-1804-44a5-8f3c-26e6585f9e95)
![Screenshot (191)](https://github.com/user-attachments/assets/13c52870-0341-4fc7-afad-63660af06418)
![Screenshot (193)](https://github.com/user-attachments/assets/03629b67-e6e1-4335-9ffa-dd171abc73b2)

## Lab- Screenshots
![VirtualBox_vsdworkshop_27_04_2025_14_42_42](https://github.com/user-attachments/assets/07e1bac8-7c8e-4c66-90b2-94b4d3e6865c)
![VirtualBox_vsdworkshop_26_04_2025_15_50_09](https://github.com/user-attachments/assets/6b0e8b93-029b-452f-a356-468b5ab7b635)
![VirtualBox_vsdworkshop_27_04_2025_14_25_04](https://github.com/user-attachments/assets/e81195be-0f76-4c27-91b9-21e12bf50184)
![VirtualBox_vsdworkshop_26_04_2025_15_56_13](https://github.com/user-attachments/assets/74be0351-40f2-4acd-8ca9-771c001871aa)
![VirtualBox_vsdworkshop_27_04_2025_14_38_44](https://github.com/user-attachments/assets/29d82d17-0b37-43a9-b849-82f914a0451f)
![VirtualBox_vsdworkshop_27_04_2025_14_39_17](https://github.com/user-attachments/assets/a58c6454-3b01-4f97-ac96-6a015c15af1b)
![VirtualBox_vsdworkshop_27_04_2025_14_41_45](https://github.com/user-attachments/assets/6a47db24-39c0-4124-8c13-132d86e2d197)
![VirtualBox_vsdworkshop_27_04_2025_14_53_36](https://github.com/user-attachments/assets/e3160d72-e42b-4c54-a85d-922739023847)

📌 Key Learnings:
 1) Floorplanning is a crucial stage that defines the chip's physical structure

 2) LEF/DEF files help in transitioning between logical and physical views of a design

 3) Special cells ensure reliability, manufacturability, and electrical correctness

  4) Placement quality directly impacts timing, congestion, and chip performance

💡 Reflection:

  Day 2 focused heavily on physical organization, setting the stage for successful routing and performance optimization later. Understanding LEF/DEF and seeing how physical rules are applied was eye-opening. Proper floorplanning and placement are critical to achieving good PPA (Power, Performance, Area) targets.

## 🟢 Day 3: Standard Cell Design & Characterization

---

### 📘 Topics Covered:

- Standard Cell Design using **Sky130 PDK**
- Schematic creation and simulation using **Ngspice**
- Understanding the structure and components of a standard cell (e.g., inverter)
- Performing **SPICE simulation** to verify cell functionality
- Introduction to **Standard Cell Characterization** (timing, power, functionality) 

### 🔧 Activities Performed:

1. **Designed a Standard Inverter Cell**  
   - Created schematic in **Xschem** using Sky130 transistors  
   - Connected PMOS and NMOS with appropriate sizing  
   - Added VDD, GND, and input/output pins

2. **Simulated the Cell using Ngspice**  
   - Wrote `.spice` netlist for the inverter  
   - Performed transient simulation to observe inverter switching behavior  
   - Verified logic functionality (Vin vs Vout)

3. **Started Cell Characterization**  
   - Measured key timing parameters:
     - Propagation delay (tpHL, tpLH)
     - Rise/fall times
     - Noise margins
   - Optionally observed power consumption using waveform analysis

## Screenshots
  ![Screenshot (195)](https://github.com/user-attachments/assets/fa4e82cf-5c9f-4fe9-b3f7-6955ddba2afd)
  ![Screenshot (196)](https://github.com/user-attachments/assets/a6e7347e-af0b-4f93-b064-7cb2fc8815fe)
  ![Screenshot (197)](https://github.com/user-attachments/assets/9e5c2714-1d39-4eb2-bc70-6afb0096166d)

## Lab- Screenshots
![VirtualBox_vsdworkshop_30_04_2025_12_47_02](https://github.com/user-attachments/assets/7e454933-adc3-4e26-bd95-1770f0315761)
![VirtualBox_vsdworkshop_30_04_2025_12_48_38](https://github.com/user-attachments/assets/0a0c49ea-1e3a-45fe-8497-4e9b0fc94c4e)
![VirtualBox_vsdworkshop_30_04_2025_12_48_50](https://github.com/user-attachments/assets/b20ce51e-20e7-4dbf-9631-4cdf4fea0562)
![VirtualBox_vsdworkshop_30_04_2025_13_17_12](https://github.com/user-attachments/assets/caab88e2-8b49-4351-9d7c-e77296cecae6)
![VirtualBox_vsdworkshop_30_04_2025_14_52_47](https://github.com/user-attachments/assets/6c94aa87-0ebd-4e9c-b9a6-f8c2801bc46c)
![VirtualBox_vsdworkshop_30_04_2025_14_53_58](https://github.com/user-attachments/assets/cd4b5f35-bc62-4722-b31a-b146bb7ad6da)
![VirtualBox_vsdworkshop_30_04_2025_15_10_40](https://github.com/user-attachments/assets/d4ac48ad-134f-4765-924d-280961fb5364)
![VirtualBox_vsdworkshop_30_04_2025_15_11_10](https://github.com/user-attachments/assets/b1536ce8-b5d2-4811-9ed5-d9ce6a7049ff)
![VirtualBox_vsdworkshop_30_04_2025_15_13_06](https://github.com/user-attachments/assets/d151d9a8-d9e0-4777-a78a-250aa1b2f3f8)
![VirtualBox_vsdworkshop_30_04_2025_15_14_56](https://github.com/user-attachments/assets/1fd1247f-fc6a-4e09-b849-8ef01d45018c)

## LAB-TASK:

Rise transition time calculation:

Rise transition time = Time taken for output to rise to 80% − Time taken for output to rise to 20%

20% of output = 660 mV
80% of output = 2.64 V

Rise transition time = 0.05868ns = 58.6ps

Fall transition time calculation:

Fall transition time = Time taken for output to fall to 20% − Time taken for output to fall to 80%

20% of output = 660 mV
80% of output = 2.64 V

Fall transition time = 0.0735ns = 73.5ps

Propagation delay calculation:
propagation delay=0.03148ns=31.4ps
![Screenshot (198)](https://github.com/user-attachments/assets/ef53f86a-78d2-41ff-ad42-e4ea7b956c56)

![VirtualBox_vsdworkshop_30_04_2025_16_08_38](https://github.com/user-attachments/assets/3fbf6092-fb9a-49bd-8ec4-d7ce08791960)
![VirtualBox_vsdworkshop_30_04_2025_16_08_46](https://github.com/user-attachments/assets/8dc30358-f851-4951-bf93-92d26f29ca65)
![VirtualBox_vsdworkshop_30_04_2025_16_13_22](https://github.com/user-attachments/assets/f8036be9-19b5-4396-bceb-0a3e74c23184)

📈 Output Observations:

  V(in) and V(out) waveforms showed clear inversion behavior

  Delays and transitions were dependent on transistor sizing and load

  Learned how electrical characteristics of basic gates are extracted

📌 Key Learnings:

  Understood how standard cells are built from transistors using PDK models

  Learned to validate circuit functionality with SPICE simulation

  Gained insight into the critical parameters used for standard cell characterization

 Recognized how these cells form the base for larger digital systems

💡 Reflection:

Day 3 shifted the focus to the analog foundation of digital design. Designing and simulating an inverter at the transistor level gave me a deeper appreciation for what goes inside a "standard cell". This hands-on experience with SPICE and Sky130 helped bridge the gap between digital abstraction and physical behavior.

## 🟢 Day 4: Timing Analysis & Clock Tree Synthesis (CTS)

---

### 📘 Topics Covered:

- Introduction to **Clock Tree Synthesis (CTS)**
- Understanding clock distribution challenges
- Performing **PnR with custom standard cells**
- Basics of **Static Timing Analysis (STA)**
- Introduction to **Timing ECOs 

### 🔧 Activities Performed:

1. **Custom Cell Integration**  
   - Used a pre-characterized or manually designed custom cell  
   - Ensured proper LEF/DEF views and timing models were included  
   - Verified placement and connectivity of the custom cell within OpenLane flow

2. **Clock Tree Synthesis Execution**  
   - Ran the CTS stage to create a balanced clock distribution network  
   - Placed buffers and inverters to manage clock skew and delay  
   - Observed the clock tree structure generated by OpenLane

3. **Static Timing Analysis (STA)**  
   - Used OpenSTA to evaluate setup and hold timing of paths  
   - Analyzed reports to identify critical paths and slack violations  
   - Checked timing paths before and after CTS

4. **Timing ECO (Engineering Change Orders)**  
   - Briefly explored how manual fixes or re-synthesis steps can fix timing violations  
   - Understood that ECOs allow patching critical issues post-synthesis

## Screenshots:
![Screenshot (199)](https://github.com/user-attachments/assets/4bea965f-5057-4839-b3c5-4d79727e678c)
![Screenshot (200)](https://github.com/user-attachments/assets/9f15cad9-73dc-4ff3-812a-ab7da665d9e4)
![Screenshot (201)](https://github.com/user-attachments/assets/c8442037-167e-46a0-954f-4571a62d77b3)
![Screenshot (202)](https://github.com/user-attachments/assets/3fc0e523-fae3-4a8a-b672-bfd0bcde7359)

## LAB-SCREENSHOTS:
![VirtualBox_vsdworkshop_02_05_2025_12_39_51](https://github.com/user-attachments/assets/38b4ae53-98c7-4878-8ae2-4d626931d885)
![VirtualBox_vsdworkshop_02_05_2025_12_34_20](https://github.com/user-attachments/assets/b7b31091-17cd-4314-a0b2-5bcf30b3858c)
![VirtualBox_vsdworkshop_02_05_2025_12_51_38](https://github.com/user-attachments/assets/e0416baa-340c-47aa-8c9e-afd7a109266a)
![VirtualBox_vsdworkshop_02_05_2025_12_41_32](https://github.com/user-attachments/assets/ab5595d5-0c99-4178-9aaf-ef32d716203a)
![VirtualBox_vsdworkshop_02_05_2025_12_43_59](https://github.com/user-attachments/assets/317f0335-bf8f-4e96-a8f1-0c75cdfb9a5c)
![VirtualBox_vsdworkshop_02_05_2025_12_53_46](https://github.com/user-attachments/assets/444a51c9-9012-4af8-84cc-18d5fab6b8f9)
![VirtualBox_vsdworkshop_02_05_2025_13_04_12](https://github.com/user-attachments/assets/757ba114-9d8a-49a3-b9b8-095be4babc76)
![VirtualBox_vsdworkshop_02_05_2025_13_23_39](https://github.com/user-attachments/assets/a2a6915d-7112-4cc0-b6e9-ebe9a1e12582)
![VirtualBox_vsdworkshop_02_05_2025_13_25_52](https://github.com/user-attachments/assets/bcc87960-2b4f-4e22-bead-f50bf1d00ffa)
![VirtualBox_vsdworkshop_02_05_2025_14_27_53](https://github.com/user-attachments/assets/506ef7ab-296d-4e1c-9f6d-9d1b2b08df65)
![VirtualBox_vsdworkshop_02_05_2025_14_28_06](https://github.com/user-attachments/assets/ba29e807-69f8-4db5-b45f-ff440232af6d)
![VirtualBox_vsdworkshop_02_05_2025_14_33_15](https://github.com/user-attachments/assets/652a7222-91ac-45c7-9f1c-442bc19f1cd7)
![VirtualBox_vsdworkshop_02_05_2025_16_07_35](https://github.com/user-attachments/assets/0286f135-756f-4b1b-97e3-8f1de0f7a87c)
![VirtualBox_vsdworkshop_02_05_2025_16_08_04](https://github.com/user-attachments/assets/83c6fc1a-4c8c-46e1-97e3-8ccd52099adc)
![VirtualBox_vsdworkshop_02_05_2025_16_22_52](https://github.com/user-attachments/assets/e0c445ad-fd0d-4831-ba94-7058124d4936)

📈 Output Files Observed:

 cts/ directory containing:

    cts.log – Log for clock tree generation

    cts.def – Layout including inserted clock buffers/inverters

 STA reports:

    timing.rpt – Timing summary

    setup.rpt / hold.rpt – Setup/hold analysis

     slack values showing path timing margins

📌 Key Learnings:

   Clock tree design is essential to balance clock arrival times across sequential elements

   CTS helps reduce clock skew and improve timing closure

   STA is critical to validate if the design meets timing constraints under all conditions

   Timing ECOs allow late-stage fixes without full re-synthesis, saving time

💡 Reflection:

 Day 4 emphasized the importance of timing in digital design. Clock Tree Synthesis showed me how crucial it is to distribute the clock uniformly to avoid skew. Using OpenSTA to analyze timing gave me hands-on experience in timing verification, and the idea of ECOs taught me that physical design is iterative and timing closure is rarely achieved in the first go.

## 🟢 Day 5: RTL-to-GDS Flow Completion


### 📘 Topics Covered:

- Introduction to **Routing** in the RTL-to-GDSII flow
- Understanding the algorithm behind **TritonRoute**
- Performing **SPEF extraction and analysis**
- Finalizing the complete ASIC design flow from RTL to GDS

### 🔧 Activities Performed:

1. **Detailed Routing with TritonRoute**  
   - Performed **global and detailed routing** of standard cells, macros, and special nets  
   - TritonRoute automatically handled wire length, spacing, DRC rules, and via generation  
   - Checked for routing congestion and DRC violations

2. **Understanding TritonRoute Algorithm**  
   - Based on A*-search and maze routing  
   - Focuses on timing-aware and DRC-clean routing paths  
   - Supports multi-layer routing and handles congestion efficiently

3. **SPEF (Standard Parasitic Exchange Format) Extraction**  
   - Extracted **RC parasitic data** from routed netlists  
   - Used for post-layout timing analysis  
   - Observed how interconnect parasitics affect real performance

4. **Final GDSII Generation**  
   - Exported GDSII layout for tapeout  
   - Ensured layout passed all checks (DRC, LVS)

## Screenshots:
![Screenshot (203)](https://github.com/user-attachments/assets/97d74bc2-1080-44e1-94b6-71f57dab1cd7)
![Screenshot (204)](https://github.com/user-attachments/assets/4fdb9a25-63ca-412e-8af5-323007363223)

## LAB-SCREENSHOTS:
![VirtualBox_vsdworkshop_02_05_2025_16_37_01](https://github.com/user-attachments/assets/7b8e3fd5-29de-4c21-9ed2-a03581a3a414)
![Screenshot (206)](https://github.com/user-attachments/assets/c67c1031-5c47-4851-ba77-5da2daab0ca3)
![VirtualBox_vsdworkshop_02_05_2025_17_17_41](https://github.com/user-attachments/assets/9d6ccc1d-9675-4752-8334-c52a495ac097)
![Screenshot (207)](https://github.com/user-attachments/assets/6d3b6ed7-9a9b-45c0-8698-2621132aee54)

📈 Output Files Observed:

 routing/ folder:

    final.def – Routed design DEF

    final.gds – Complete layout for tapeout

    route.log – Routing execution details

 spef/ folder:

    design.spef – File with parasitic RC info

    Post-route timing reports

📌 Key Learnings:

  Routing connects the entire logic physically and is a critical final step before tapeout

  TritonRoute ensures optimal, DRC-compliant routing across multiple layers

  Parasitic effects (RC) must be analyzed using SPEF for accurate timing

  RTL-to-GDS is a multi-step process requiring checks and optimization at every stage

💡 Reflection:

Day 5 marked the culmination of the RTL-to-GDSII journey. Understanding how routing and parasitic extraction wrap up the physical design helped me appreciate the complexity of a real ASIC design. From writing RTL to viewing a manufacturable GDSII layout — this workshop gave me end-to-end exposure.

##  Acknowledgment:

I would like to express my sincere gratitude to **VLSI System Design (VSD) Program** for organizing this hands-on workshop on Physical Design using **OpenLane** and **Sky130 PDK**.

This 2-weeks journey has been an enriching experience, offering practical exposure to the complete RTL-to-GDSII flow. The workshop not only deepened my understanding of physical design concepts like synthesis, placement, CTS, routing, and timing analysis but also provided a platform to work with industry-grade open-source tools.

Special thanks to **Kunal Ghosh**, **VSD team**, and all the mentors who made complex topics accessible through structured sessions and labs.

This experience has strengthened my interest in VLSI design and has equipped me with valuable skills for my future in semiconductor engineering.









































