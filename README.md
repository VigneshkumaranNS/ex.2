### Ex. No. : 2 
### Date: 31.3.23 
# Implementation of Combinational logic circuit using Verilog HDL
## Aim:
To implement the following Boolean functions using Verilog HDL and to verify the truth table.
1. F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D
2. F2=xy’z+x’y’z+w’xy+wx’y+wxy

## Components Required:
1.	Laptop with Quartus software and modelsim software.

## Theory:
Combinational Logic Circuits are memoryless digital logic circuits whose output at any instant in time depends only on the combination of its inputs.
The outputs of Combinational Logic Circuits are only determined by the logical function of their current input state, logic “0” or logic “1”, at any given instant in time.

![image](https://github.com/rvinifa/ex.2/assets/133735746/949815d3-0912-49c7-81c0-eea1c148d48e)

The result is that combinational logic circuits have no feedback, and any changes to the signals being applied to their inputs will immediately have an effect at the output. In other words, in a Combinational Logic Circuit, the output is dependant at all times on the combination of its inputs. Thus, a combinational circuit is memoryless.

## Procedure:
1.	Type the program in Quartus software.
2.	Compile and run the program.
3.	Generate the RTL schematic and save the logic diagram.
4.	Create nodes for inputs and outputs to generate the timing diagram.
5.	For different input combinations, generate the timing diagram.

## Simplification:

## Truth Table:
![de2 2](https://github.com/VigneshkumaranNS/ex.2/assets/119484483/8221ec02-63d5-47e5-ae76-d8f5afa56e85)
![de2 3](https://github.com/VigneshkumaranNS/ex.2/assets/119484483/c213af82-7011-4b10-9d13-a93ac40bf2c0)

## Program:
```
module exp2a(a,b,c,d,f1,f2);
input a,b,c,d;
output f1,f2;
wire adash,bdash,cdash,ddash,x,y,z,p,q,r;
not(adash,a);
not(bdash,b);
not(cdash,c);
not(ddash,d);
and(x,bdash,ddash);
and(y,adash,b,d);
and(z,a,b,cdash);
or(f1,x,y,z);
and(p,cdash,d);
and(q,a,c);
and(r,b,c);
or(f2,p,q,r);
endmodule
```

## RTL Schematic:
![Screenshot 2023-06-09 143954](https://github.com/VigneshkumaranNS/ex.2/assets/119484483/c5231eec-8f13-4808-8807-69d6a12c7e2c)



## Timing Diagram:
![Screenshot 2023-06-09 144007](https://github.com/VigneshkumaranNS/ex.2/assets/119484483/6540d9ea-e2a0-487b-b0c6-f8243c7e9f7f)




## Result:

Thus the given Boolean functions are implemented in Verilog HDL and the truth table are verified.



