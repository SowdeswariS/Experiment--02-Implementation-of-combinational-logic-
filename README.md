## Name: S Sowdeswari
## Register number: 212223050051

# Experiment--02-Implementation-of-combinational-logic

Implementation of combinational logic gates

 
## AIM:


To implement the given logic function verify its operation in Quartus using Verilog programming.
 F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D
F2=xy’z+x’y’z+w’xy+wx’y+wxy
 
 
## Equipments Required:
 Hardware – PCs, Cyclone II , USB flasher
 
 Software – Quartus prime


## Theory:


 A combinational circuit is a circuit in which the output depends on the present combination of inputs.
Combinational circuits are made up of logic gates. The output of each logic gate is determined by its logic
function. Combinational circuits can be made using various logic gates, such as AND gates, OR gates, and NOT
gates.


## Procedure:

Create a New Design File:
1. Create a New Project:
• Open Quartus and create a new project by selecting "File" > "New Project Wizard."
• Follow the wizard's instructions to set up your project, including specifying the project name, location,
and target device (FPGAL
2. Create a New Design File:
• Once the project is created, right-click on the project name in the Project Navigator and select "Add New
File
• Choose "Verilog HDL File" or "VHDL File, depending on your chosen hardware description language.
3. Write the Combinational Logic Coder:
• Open the newly created Verilog or VHDL file and write the code for your combinational logic.
4. Compile the Project:
• To compile the project, click on "Processing"> "Start Compilation" in the menu.
• Quartus will annlayse your code, systhesis it into a netlist, and perform optimizatioons based on your
target FGPA device
5. Analyze and Fix Errors:
• If there are any errors or warnings during the compilation process, Quartus will display them in the
Messages window.
• Review and fix any issues in your code if necessary.
• View the RTL diagram
6. Verifications:
• Click on "The "New"> "Verification/Debugging Files" > "University Program VWF".
• Once Waveform is created flight Click on the Input/Output Panel > "Insert Node or Bus" > Click on Node
Finder > Click On "List"> Select All
• Give the Input Combinations according to the Truth Table and then simulate the Output waveform


## Program:

module combination(a,b,c,d,F);

input a,b,c,d;

output F;

wire x1,x2,x3,x4,x5;

assign x1=(~a)&(~b)&(~c)&(~d);

assign x2=(a)&(~c)&(~d);

assign x3=(~b)&(c)&(~d);

assign x4=(~a)&(b)&(c)&(d);

assign x5=(b)&(~c)&(d);

assign F=x1|x2|x3|x4|x5;

endmodule


## RTL realization


![Screenshot 2023-12-24 085923](https://github.com/SowdeswariS/Experiment--02-Implementation-of-combinational-logic-/assets/154341385/3b1cf523-6c8b-4bf1-bc55-65c6d7f065b0)



## Truth table:



![Screenshot 2023-12-24 112625](https://github.com/SowdeswariS/Experiment--02-Implementation-of-combinational-logic-/assets/154341385/e206b6bb-ea4d-4751-bb3f-d6078b99bfb3)



## Timing Diagram


![Screenshot 2023-12-24 112642](https://github.com/SowdeswariS/Experiment--02-Implementation-of-combinational-logic-/assets/154341385/470a9cf8-1d6b-4f5b-8c09-d27f7d11f21f)


## Result:
Thus the given logic functions are implemented using  and their operations are verified using Verilog programming.
