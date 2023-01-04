# Experiment--03-Half-Subtractor-and-Full-subtractor
## Implementation-of-Half-subtractor-and-Full-subtractor-circuit
## AIM:
To design a half subtractor and full subtractor circuit and verify its truth table in Quartus using Verilog programming.

## Equipments Required:
## Hardware – PCs, Cyclone II , USB flasher
## Software – Quartus prime
## Theory
Subtractor circuits take two binary numbers as input and subtract one binary number input from the other binary number input. Similar to adders, it gives out two outputs, difference and borrow (carry-in the case of Adder). There are two types of subtractors.

## Half Subtractor Full Subtractor
## Half Subtractor
The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed.
![half-subtractor9](https://user-images.githubusercontent.com/36288975/166112538-58c3bc7c-ee5d-4e6a-ac8d-8e8328efe27a.png)


Sum = X'Y+XY' = X ⊕ Y
Carry=X'Y

## Full Subtractor
A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow. 
![full-subtractor6](https://user-images.githubusercontent.com/36288975/166112541-24c68359-3de8-4674-ae22-8272ffc385ed.png)


Diff = A ⊕ B ⊕ Bin B = A'Bin + A'B + BBin

## Procedure



Write the detailed procedure here 


## Program:
/*
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by: M.PRAKASH.
RegisterNumber:22009001  
*/


HALF SUBTRACTOR:

module halfsub(A,B,Diff,borr);
input A,B;
output Diff,borr;
assign Diff = (A ^ B);
assign borr = (~ A & B);
endmodule


FULL SUBTRACTOR:

module EX3 (A,B,C,Diff,Borrow);\n
input A,B,C;\n
output Diff,Borrow;\n
assign Borrow=(~A&(B ^ C) | (B & C));\n
assign Diff=(A ^ B ^ C);\n
endmodule

## Truthtable
HALF SUBTRACTOR truth table:
![image](https://user-images.githubusercontent.com/118350045/210563714-2902033f-f97e-4aab-8a35-30c3aace70b1.png)
Full subtractor truth table:
![image](https://user-images.githubusercontent.com/118350045/210565499-25f725bd-595f-40cf-be2f-e8a1001efee5.png)



##  RTL realization

Half Subtractor:
![Screenshot_20230104_063803](https://user-images.githubusercontent.com/118350045/210565968-4b996478-ce1a-4007-a348-a3967eabc7c1.png)

Full Subtractor:
![Screenshot_20230104_022616](https://user-images.githubusercontent.com/118350045/210566231-bb830fe7-5be1-40fb-8b0e-8fc224c80770.png)



## Timing diagram 
Half Subtractor:
![image](https://user-images.githubusercontent.com/118350045/210566492-93785771-38fe-4e3a-a012-b9dba5277fa7.png)

Full Subtractor:
![image](https://user-images.githubusercontent.com/118350045/210566903-89c55bd5-b357-47b7-ad2f-3d0408418a26.png)


## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
