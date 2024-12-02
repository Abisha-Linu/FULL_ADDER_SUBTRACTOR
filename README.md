# FULL_ADDER_SUBTRACTOR

Implementation-of-Full-Adder-and-Full-subtractor-circuit

**AIM:**

To design a Full Adder and Full Subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher

Software – Quartus prime

**Full Adder and Full Subtractor**

**Full Adder**

Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin 

Carry = AB + ACin + BCin

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/0f30ba51-5ffb-4198-845f-18e054f675e7)

**Figure -1 FULL ADDER**

**Full Subtractor**

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/02b24f51-ab51-4304-9ad6-7b81ffc1ead5)

Diff = A ⊕ B ⊕ Bin 

Borrow out = A'Bin + A'B + BBin

**Truthtable**

![image](https://github.com/user-attachments/assets/1020568c-7bd7-4e86-b90d-ac1d3ed5a08f)

![image](https://github.com/user-attachments/assets/3388fd64-c6c8-427c-9992-2f13465e8884)

**Procedure**

 Full Adder: Inputs: Three inputs: A, B (the two bits to be added), and Cin (the carry-in bit from a
 previous addition). Outputs: Two outputs: Sum (the resulting sum) and Cout (the carry-out bit).
 Logic: Sum = A ^ B ^ Cin (XOR operation). Cout = (A & B) | (A & Cin) | (B & Cin) (carry occurs if at
 least two inputs are 1).
 Full Subtractor: Inputs: Three inputs: A, B (the two bits, where A - B is calculated), and Bin (the
 borrow-in from a previous subtraction). Outputs: Two outputs: Diff (the resulting difference) and
 Bout (the borrow out bit). Logic: Diff = A ^ B ^ Bin (XOR operation). Bout = (~A & B) | ((~A | B) &
 Bin) (borrow occurs if A is less than B or needs a borrow). Both circuits follow simple XOR logic for
 the primary result and AND-OR logic to determine carry or borrow conditions
 
**Program:**
```
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by:Abisha Linu.L
RegisterNumber:24900028

```
```
 module fulladdsub(a,b,cin,bin,sum,carry,difference,borrow); 
input a,b,cin,bin; output sum,carry,difference,borrow; 
assign sum=a^b^cin; 
assign carry=(a^b)&cin|a&b;
 assign difference=a^b^bin; 
assign borrow=~(a^b)&bin|(~a)&b;
```
**RTL Schematic**

![image](https://github.com/user-attachments/assets/48e763cd-2de5-4853-b4a6-fb7a91b1eeb7)

**Output Timing Waveform**

![image](https://github.com/user-attachments/assets/0263b286-88f0-4443-b01a-087cb9f51918)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



