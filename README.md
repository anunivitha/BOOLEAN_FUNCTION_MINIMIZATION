# BOOLEAN_FUNCTION_MINIMIZATION

**AIM:**

To implement the given logic function verify its operation in Quartus using Verilog programming.

F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D 

F2=xy’z+x’y’z+w’xy+wx’y+wxy

**Equipment Required:**

Hardware – PCs, Cyclone II , USB flasher

**Software – Quartus prime**

**Theory**

**Logic Diagram**

**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**

/* Program to implement the given logic function and to verify its operations in quartus using Verilog programming. 

Developed by: Anu Nivitha U
RegisterNumber: 212223040016 
*/
```
module Boolean_min(A,B,C,D,W,X,Y,Z,F1,F2);
input A,B,C,D,W,X,Y,Z;
wire x1,x2,x3,x4,x5,x6,x7,x8,x9,x10;
output F1,F2;
assign x1=(~A)&(~B)&(~C)&(~D);
assign x2=(A)&(~C)&(~D);
assign x3=(~B)&(C)&(~D);
assign x4=(~A)&(B)&(C)&(D);
assign x5=(B)&(~C)&(D);
assign x6=(X)&(~Y)&(Z);
assign x7=(~X)&(~Y)&(Z);
assign x8=(~W)&(X)&(Y);
assign x9=(W)&(~X)&(Y);
assign x10=(W)&(X)&(Y);
assign F1=x1|x2|x3|x4|x5;
assign F2=x6|x7|x8|x9|x10;
endmodule
```

** Logic symbol & Truthtable: **
<img width="684" alt="Screenshot 2025-05-31 at 9 51 00 PM" src="https://github.com/user-attachments/assets/af2ebe48-06b6-4173-a4da-0866c4871c4d" />
<img width="682" alt="Screenshot 2025-05-31 at 9 51 06 PM" src="https://github.com/user-attachments/assets/412ae6a2-63d4-4803-a6ec-a12f1a296d87" />


**RTL realization**

**Output:**

**RTL**
<img width="523" alt="Screenshot 2025-05-31 at 9 51 12 PM" src="https://github.com/user-attachments/assets/a9a65392-9b33-4c25-9d24-53b440b72291" />

**Timing Diagram**
<img width="707" alt="Screenshot 2025-05-31 at 9 51 17 PM" src="https://github.com/user-attachments/assets/2436e6de-058f-4cc1-9a9f-af854916ed2e" />


**Result:**

Thus the given logic functions are implemented using and their operations are verified using Verilog programming.

