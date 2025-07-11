# Physical-Design-flow-of-the-RISC-V-Processor-using-32nm-Technology

TOOLS HANDLED

Tool :  DC Compiler (DC) 
For Synthesis to convert RTL code into Gatelevel Netlist
Used for Synthesizing ALU, Machine Counter and Top Module Netlists
Input 		: Verilog/VHDL RTL
Output		: Gate-level netlist (.v), reports

Tool : IC Compiler II (ICCII)
Place and Route (PnR) takes the synthesized netlist and implements the physical layout of the design.
Implementing PnR for ALU and Machine Counter. Full-chip PnR of the Top Module
Input		: Netlist (.v), .lib, .tf, .lef, .tluplus
Output	: GDSII, layout views

Tool : LM_SHELL
Used to create and manage Milkyway libraries (used in ICCII).
Helps in creating Hard Macros (pre-placed-and-routed blocks).
Input		: .tf, .db, .lef
Output	: Milkyway database (.mw)

PROJECT FLOW

1 .Hard Macro Creation of ALU 			          Using DC + ICCII + LM_SHELL
2. Hard Macro Creation of Machine Counter 		Using DC + ICCII + LM_SHELL
3. TOP Module Synthesis 			              	Using Design Compiler (DC)
4. Top Module PnR Implementation 			      Using ICCII


