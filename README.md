# Experiment--02-Implementation-of-combinational-logic
Implementation of combinational logic gates
 
## AIM:
To implement the given logic function verify its operation in Quartus using Verilog programming.
 F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D
F2=xy’z+x’y’z+w’xy+wx’y+wxy
 
 
 
## Equipments Required:
## Hardware – PCs, Cyclone II , USB flasher
## Software – Quartus prime


## Theory
 Logic gates are electronic circuits which perform logical functions on one or more inputs to produce one output.

## Logic Diagram

Using NOR gates NOR gate is actually a combination of two logic gates: OR gate followed by NOT gate. So its output is complement of the output of an OR gate. This gate can have minimum two inputs, output is always one. By using only NOR gates, we can realize all logic functions: AND, OR, NOT, Ex-OR, Ex-NOR, NAND. So this gate is also called universal gate. Designing a circuit with NOR gates only uses the same basic techniques as designing a circuit with NAND gates; that is, the application of deMorgan’s theorem. The only difference between NOR gate design and NAND gate design is that the former must eliminate product terms and the later must eliminate sum terms.

F=(((C.B'.A)+(D.C'.A)+(C.B'.A))')'

## Procedure

   # 1 Create a project with required entities.
   # 2 Create a module along with respective file name.
   # 3 Run the respective programs for the given boolean equations.
   # 4 Run the module and get the respective RTL outputs.
   # 5 Create university program(VWF) for getting timing diagram.
   # 6 Give the respective inputs for timing diagram and obtain the results.


## Program:

Program to implement the given logic function using NAND and NOR gates and to verify its operations in quartus using Verilog programming.

Developed by: VIJAYARAJ V

RegisterNumber:  212222230174

using NAND:
   
   module combo1(a,b,c,d,f);
   
   input a,b,c,d;
   
   output f;
   
   wire p,q,r;
   
   assign p=(~c & b & a);
   
   assign q=(~d & c & ~a);
   
   assign r=(c & ~b & a);
   
   assign f=(~(~p & ~q & ~r));
   
   endmodule

using NOR:

   module combo2(a,b,c,d,f);
   
   input a,b,c,d;
   
   output f;
   
   wire p,q,r;
   
   assign p=( c & ~b & a);
   
   assign q=( d & ~c & a);
   
   assign r=( c & ~b & a);
   
   assign f=(~(~( p | q | r)));
   
   endmodule
   
## RTL realization
## Output:
## RTL

![image](https://user-images.githubusercontent.com/121303741/234763437-51ee228a-8674-440f-bb71-b56f67558471.png)

## Timing Diagram

![image](https://user-images.githubusercontent.com/121303741/234763498-18363a27-5503-42f1-9cf0-c423e54726e1.png)

## Time Table

![image](https://user-images.githubusercontent.com/121303741/234763584-1a6e12a6-3710-4f89-8048-fec3484498c5.png)

## Use NOR:

![image](https://user-images.githubusercontent.com/121303741/234763713-1b98a52e-1067-49ba-86be-2f0a107dcb1c.png)

## Timing Diagram:

![image](https://user-images.githubusercontent.com/121303741/234763784-58f553a8-4038-4bca-b77e-43f55cf54603.png)

## Truth Table:

![image](https://user-images.githubusercontent.com/121303741/234763843-6d99b7c3-9d04-4b29-9dc2-5aedd5a0dfbf.png)

## Result:
Thus the given logic functions are implemented using  and their operations are verified using Verilog programming.
