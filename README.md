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










