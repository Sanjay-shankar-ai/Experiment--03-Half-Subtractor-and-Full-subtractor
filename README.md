# Experiment--03-Half-Subtractor-and-Full-subtractor

## Implementation-of-Half-subtractor-and-Full-subtractor-circuit

## AIM:

To design a half subtractor and full subtractor circuit and verify its truth table in Quartus using Verilog programming.

## Equipments Required:

Hardware – PCs, Cyclone II , USB flasher.

Software – Quartus prime.

## Theory:

Subtractor circuits take two binary numbers as input and subtract one binary number input from the other binary number input. Similar to adders, it gives out two outputs, difference and borrow (carry-in the case of Adder). There are two types of subtractors.

## Half Subtractor Full Subtractor:

## Half Subtractor:

The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed.

![half-subtractor9](https://user-images.githubusercontent.com/36288975/166112538-58c3bc7c-ee5d-4e6a-ac8d-8e8328efe27a.png)


Sum = X'Y+XY' = X ⊕ Y

Carry=X'Y

## Full Subtractor:

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow. 

![full-subtractor6](https://user-images.githubusercontent.com/36288975/166112541-24c68359-3de8-4674-ae22-8272ffc385ed.png)


Diff = A ⊕ B ⊕ Bin B = A'Bin + A'B + BBin


## Procedure:

1. Use module projname(input,output) to start the Verilog programmming.

2. Assign inputs and outputs using the word input and output respectively.

3. Use defined keywords like wire,assign and required logic gates to represent the boolean expression.

4. Use each output to represnt onre for differnce and the other for borrow.

5. End the verilog program using keyword endmodule.


## Program:

Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.

```c

Developed by: Sanjay. S
Register Number:  212221230086


HALF SUBTRACTOR:

module HalfSubtractor(A,B,Diff,Borrow);
input A,B;
output Diff,Borrow;
wire x;
xor (Diff, A,B);
not(x,A);
and(Borrow,x,B);
endmodule

FULL SUBTRACTOR:

module FullSubtractor(A,B,C,Diff,Borrow);
input A,B,C;
output Diff,Borrow;
wire p;
assign Diff = ((A^B)^C);
not(p,A);
assign Borrow = ((p&B)|(p&C)|(B&C));
endmodule

```

## Output

## Half Subtractor

## Logic Symbol


![img1](https://user-images.githubusercontent.com/94231938/232325709-ce75376e-67a6-421d-953b-305ad206a448.png)


## Truthtable


![img2](https://user-images.githubusercontent.com/94231938/232325711-6bbf0188-db2e-43b6-8a1e-2994904a9ba9.png)


##  RTL realization

![img3](https://user-images.githubusercontent.com/94231938/232325717-ac675adc-4a7d-46d5-9ace-0a44207cb488.png)



## Timing diagram 


![img4 (2)](https://user-images.githubusercontent.com/94231938/232325722-8a6cebba-e59b-42f0-8f2e-e74d0f03e220.png)


## Full Subtractor

## Logic Symbol


![img5 (2)](https://user-images.githubusercontent.com/94231938/232325724-117b90ca-7c50-4aad-b02d-f485973b1c6c.png)


## Truthtable


![img6 (2)](https://user-images.githubusercontent.com/94231938/232325728-924e9082-859b-4d56-b412-a1a337e01dfa.png)


##  RTL realization


![img7 (2)](https://user-images.githubusercontent.com/94231938/232325729-dc38a0f5-299c-4fed-9645-cd39b312e190.png)


## Timing diagram


![img8 (2)](https://user-images.githubusercontent.com/94231938/232325731-cd351f23-11b1-4634-aa3a-e4c8aa0500a8.png)



## Result:

Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.


