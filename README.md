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
## Procedure

1.Create a project with required entities.

2.Create a module along with respective file name.

3.Run the respective programs for the given boolean equations.

4.Run the module and get the respective RTL outputs.

5.Create university program(VWF) for getting timing diagram.

6.Give the respective inputs for timing diagram and obtain the results.

## Program:

Program to implement the given logic function using NAND and NOR gates and to verify its operations in quartus using Verilog programming.

Developed by:SUDHAKAR K

RegisterNumber: 212222240107

### Program 1:
````
module expfour(a,b,c,d,f);

input a,b,c,d;

output f;

wire f1,f2,f3;

assign f1 = (~c&~b&~a);

assign f2 = (~d&~c&~a);

assign f3 = (c&~(~b)&~a);

assign f= f1&~f2&~f3;

endmodule
````
## Program 2:
````
module expfourtwo(a,b,c,d,f);

input a,b,c,d;

output f;

wire f1,f2,f3,f4;

assign f1 = c&(~b)&a;

assign f2 = d&(~c)&a;

assign f3 = c&(~b)&a;

assign f4 = ~(f1|f2|f3);

not(f,f4);

endmodule
````

## Output:

## RTL realization

Program 1:

![Screenshot (41)](https://user-images.githubusercontent.com/118799103/211163345-02893d9a-420f-4bc9-bdbd-e541514aadb1.png)

Program 2:

![Screenshot (43)](https://user-images.githubusercontent.com/118799103/211163380-9af4bdd3-ffc4-4f53-8e79-433177adf9fb.png)

## TRUTH TABLE

Program 1:

![Screenshot (45)](https://user-images.githubusercontent.com/118799103/211163433-d34c9732-158c-42b0-862b-d930970e5ffb.png)

Program 2:

![Screenshot (46)](https://user-images.githubusercontent.com/118799103/211163462-939a3b0b-150d-40aa-913c-bf4f743a3261.png)

## RTL

Program 1:

![Screenshot (48)](https://user-images.githubusercontent.com/118799103/211163497-8810043e-8bc3-492c-ba46-1cec1247be96.png)

Program 2:

![Screenshot (49)](https://user-images.githubusercontent.com/118799103/211163520-c6c8e10d-8bd8-4628-83b6-e179812faa00.png)

## Result:

Thus the given logic functions are implemented using NAND and NOR gates and their operations are verified using Verilog programming.
