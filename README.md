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















