# Experiment--04-Implementation-of-combinational-logic-using-universal-gates

Implementation of combinational logic using universal-gates

## AIM:

To implement the given logic function using NAND and NOR gates and to verify its operation in Quartus using Verilog programming.

F=((C'.B.A)'(D'.C.A)'(C.B'.A)')' using NAND gate
F=(((C.B'.A)+(D.C'.A)+(C.B'.A))')' using NOR gate

## Equipments Required:

## Hardware – PCs, Cyclone II , USB flasher

## Software – Quartus prime

## Theory

Logic gates are electronic circuits which perform logical functions on one or more inputs to produce one output.

## Using NAND gates

NAND gate is actually a combination of two logic gates i.e. AND gate followed by NOT gate. So its output is complement of the output of an AND gate.This gate can have minimum two inputs, output is always one. By using only NAND gates, we can realize all logic functions: AND, OR, NOT, X-OR, X-NOR, NOR. So this gate is also called as universal gate. First note that the entire expression is inverted and we have three terms ANDed. This means that we must use a 3-input NAND gate. Each of the three terms is, itself, a NAND expression. Finally, negated single terms can be generates with a 2-input NAND gate acting as an inverted.

F=((C'.B.A)'(D'.C.A)'(C.B'.A)')'

## Logic Diagram

Using NOR gates
NOR gate is actually a combination of two logic gates: OR gate followed by NOT gate. So its output is complement of the output of an OR gate. This gate can have minimum two inputs, output is always one. By using only NOR gates, we can realize all logic functions: AND, OR, NOT, Ex-OR, Ex-NOR, NAND. So this gate is also called universal gate. Designing a circuit with NOR gates only uses the same basic techniques as designing a circuit with NAND gates; that is, the application of deMorgan’s theorem. The only difference between NOR gate design and NAND gate design is that the former must eliminate product terms and the later must eliminate sum terms.

F=(((C.B'.A)+(D.C'.A)+(C.B'.A))')'

## Logic Diagram

![](op1.png)

## Procedure

Step-1:
Install quartus and its components.

Step-2:
Create a new project and enter the required code in verilog HDL file.

Step-3:
Compile the program and view the rtl file for logic diagram.

Step-4:
Get the timing diagram for different inputs using VWF file.

## Program:

```
/*
Program to implement the given logic function using NAND and NOR gates and to verify its operations in quartus using Verilog programming.
Developed by: Pradeesh S
RegisterNumber:  212221240038


module cc_1(a,b,c,f);
input a,b,c;
output f;
wire p,q,r;
assign p=(~a & b & c);
assign q=(a & ~b & c);
assign r=(a & b & ~c);
assign f=((p |q|r));
endmodule
*/
```

## RTL realization

## Output:

## RTL

![](op2.png)

## Timing Diagram

![](op3.jpeg)

## Result:

Thus the given logic functions are implemented using NAND and NOR gates and their operations are verified using Verilog programming.
