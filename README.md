# HALF_ADDER_SUBTRACTOR

Implementation-of-Half-Adder-and-Half Subtractor-circuit

**AIM:**

To design a half adder and half subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher 

Software – Quartus prime Theory Adders are digital circuits that carry out the addition of numbers.

**Half Adder**

Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

![image](https://github.com/naavaneetha/HALF_ADDER_SUBTRACTOR/assets/154305477/bd4a0b2c-cdbc-4184-ab08-81578f121e1f)

Figure -01 HALF ADDER

**Half Subtractor**

The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed. 

Diff = A’B+AB’ =A ⊕ B
Borrow = A’B

 ![image](https://github.com/naavaneetha/HALF_ADDER_SUBTRACTOR/assets/154305477/d76b099c-513f-4e7c-843a-e2fd028a531a)

Figure -02 HALF Subtractor

**Truthtable**
**Halfadder**
![image](https://github.com/pochireddyp/HALF_ADDER_SUBTRACTOR/assets/150232043/5f0d7b66-3c99-4e67-af8b-8609f68c9891)
**Halfsubtractor**
![image](https://github.com/pochireddyp/HALF_ADDER_SUBTRACTOR/assets/150232043/0a2577a1-9d50-41c7-9887-206bf550efe0)


**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**

Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.

**Developed by:pochireddy.p**

**RegisterNumber:212223240115**

```
module half_addsub(a,b,sum,carry,D,Bo);
input a,b;
output sum,carry , D, Bo;
xor G1(sum,a,b);
and G2(carry,a,b);
not G4(abar,a);
xor G3(D,a,b);
and G5 (Bo,abar,b);
endmodule
```
**RTL Schematic**

![image](https://github.com/pochireddyp/HALF_ADDER_SUBTRACTOR/assets/150232043/7016396c-26a7-41ea-b17f-f8c253444d0c)


**Output/TIMING Waveform**
![image](https://github.com/pochireddyp/HALF_ADDER_SUBTRACTOR/assets/150232043/d9dd26ed-8e34-4b6e-b048-b86f8aa9ee20)


**Result:**

Thus the half adder and half subtractor circuits are designed and the truth tables are verified successfully using quartus software.
