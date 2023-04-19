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
```
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by: Shankar Saradha   
RegisterNumber: 212221240052
```

``` python 
HALF SUBTRACTOR

module HalfSubtractor(A,B,Diff,Borrow);
input A,B;
output Diff,Borrow;
wire x;
xor (Diff, A,B);
not(x,A);
and(Borrow,x,B);
endmodule

FULL SUBTRACTOR

module FullSubtractor(A,B,C,Diff,Borrow);
input A,B,C;
output Diff,Borrow;
wire p;
assign Diff = ((A^B)^C);
not(p,A);
assign Borrow = ((p&B)|(p&C)|(B&C));
endmodule
```


## Output:
## Half Subtractor
## Gates
![d](https://user-images.githubusercontent.com/93978702/233147243-d2455bf6-1154-4336-9637-c97d208b7610.png)

## Truthtable
![e](https://user-images.githubusercontent.com/93978702/233147314-bb1d2392-9aba-4b36-ae9b-6b629025487f.png)



##  RTL realization
![f](https://user-images.githubusercontent.com/93978702/233147338-1709af3b-167b-4c79-8ff6-b04ecd058aa7.png)


## Timing diagram 
![g](https://user-images.githubusercontent.com/93978702/233147376-9f4d9083-8827-494e-ba7a-3d65fa19dd2b.png)
## Full Subtractor 
## Gates
![h](https://user-images.githubusercontent.com/93978702/233148020-6c3b5e03-1e70-4dca-9d9e-25bd555e4e7a.png)


## Truthtable
![i](https://user-images.githubusercontent.com/93978702/233148045-95e5d53a-3255-4b2b-8365-c429b8bdd66d.png)




##  RTL realization
![j](https://user-images.githubusercontent.com/93978702/233148060-4f678f71-5d49-4fcb-8495-842e6ccf2714.png)



## Timing diagram 
![k](https://user-images.githubusercontent.com/93978702/233148071-d852a68b-9525-49a4-a99c-3476a5b54a9b.png)



## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
