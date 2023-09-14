# Experiment--03-Half-Subtractor-and-Full-subtractor
```
Developed by: R.Jayamani
Reg no: 212222100014
```
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

Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.

Developed by: R.Jayamani

RegisterNumber: 212222100014
### Half Subtractor
```
module half(a,b,s,c);
input a,b;
output s,c;
assign s = a^b;
assign c = ~a&b;
endmodule

```
### Full Subtractor
```
module half(a,b,bin,diff,borrow);
input a,b,bin;
output diff,borrow;
assign diff = a^b^bin;
assign borrow = ~a&b | ~(a^b)&bin;
endmodule
```
## Output:

## Truthtable
### Half Subtractor
![image](https://github.com/Jayamani25/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/85949888/57da5683-4e61-49c0-80a5-e72c5f8105af)

### Full Subtractor
![image](https://github.com/Jayamani25/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/85949888/88a7a836-0468-4925-b814-063368706ecf)

##  RTL realization
### Half Subtractor
![image](https://github.com/Jayamani25/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/85949888/3e93b260-040b-4287-a38e-4229775c1363)

### Full Subtractor
![image](https://github.com/Jayamani25/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/85949888/78836198-6c45-4a16-bc42-17ae8468fa8c)


## Timing diagram 
### Half Subtractor
![image](https://github.com/Jayamani25/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/85949888/d6c2c1f7-16eb-4450-acea-c5a09ee79504)


### Full Subtractor
![image](https://github.com/Jayamani25/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/85949888/0bf8d8e0-e3e4-4477-a3e3-008cc92139be)

## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
