#### NAME:SHALINI.K
#### REG.NO:212222240095
# Experiment--04-Half-Subtractor-and-Full-subtractor
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

  1. Connect the supply (+5V) to the circuit.
  2. Switch ON the main switch.
  3. If the output is 1, then the led glows.

## Program:
```
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by: SHALINI.K
RegisterNumber: 212222240095
1. Program to design a half subtractor:

module ex4(a,b,diff,borr);
input a,b;
output diff,borr;
assign diff=(a^b);
assign borr=((~a)&b);
endmodule 

2. Program to design a full subtractor:

module ex41(a,b,bin,diff,borr);
input a,b,bin;
output diff,borr;
assign diff=a^b^bin;
assign borr=((~a)&b)|(b&bin)|((~a)&bin);
endmodule 
```

## Output:

## TRUTH TABLE:
### HALF SUBTRACTOR
![267699989-78af586e-1adf-4892-9544-04c5bfe2d3ca](https://github.com/shalinikannan23/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/118656529/99b2250e-55ce-45cd-ad25-9db8c0f146fa)

### FULL SUBTRACTOR

![267700583-a9b18974-158f-4ff9-8fc8-4d568fbf95f9](https://github.com/shalinikannan23/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/118656529/ab803902-a781-4d2f-be97-46b21b55d9c7)

##  RTL REALIZATION:
### HALF SUBTRACTOR
![267701085-7364d45f-9d82-430b-81e9-2ff55b8bd689](https://github.com/shalinikannan23/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/118656529/8bd21589-f98c-4398-98bc-2898135d725c)


### FULL SUBTRACTOR

![267701128-132fc82f-d262-4cbc-9850-86339dc4cb9b](https://github.com/shalinikannan23/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/118656529/99819672-0720-4952-8ae8-08fea5117f66)

## OUTPUT WAVEFORM:
### HALF SUBTRACTOR

![267701235-9a4af079-d35e-43e5-8690-9d390d041fb6](https://github.com/shalinikannan23/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/118656529/ae04fe59-4308-493a-8d39-dfe4b82adb12)


### FULL SUBTRACTOR
![267701298-5ea55e95-6c55-44f9-a5f8-938858e6876f](https://github.com/shalinikannan23/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/118656529/80dc956c-0d6b-4c65-a102-629474f885ee)

## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
