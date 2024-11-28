### NAME:MANIMARAN.V
### REG.NO.24008541
### EXPERIMENT 4:FULL_ADDER_SUBTRACTOR

Implementation-of-Full-Adder-and-Full-subtractor-circuit

### AIM:

To design a Full Adder and Full Subtractor circuit and verify its truth table in Quartus using Verilog programming.

### EQUIPMENTS REQUIRED:

Hardware – PCs, Cyclone II , USB flasher

Software – Quartus prime

### FULL ADDER AND FULL SUBTRACTOR

### FULL ADDER

Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin 

Carry = AB + ACin + BCin

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/0f30ba51-5ffb-4198-845f-18e054f675e7)

### FIGURE -1 FULL ADDER

### FULL SUBTRACTOR

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/02b24f51-ab51-4304-9ad6-7b81ffc1ead5)

Diff = A ⊕ B ⊕ Bin 

Borrow out = A'Bin + A'B + BBin

### PROCEDURE

Full Adder
Inputs: Three inputs: A, B (the two bits to be added), and Cin (the carry-in bit from a previous
addition). Outputs: Two outputs: Sum (the resulting sum) and Cout (the carry-out bit). Logic: Sum =
A ^ B ^ Cin (XOR operation). Cout = (A & B) | (A & Cin) | (B & Cin) (carry occurs if at least two
inputs are 1).
Full Subtractor
Inputs: Three inputs: A, B (the two bits, where A - B is calculated), and Bin (the borrow-in from a
previous subtraction). Outputs: Two outputs: Diff (the resulting difference) and Bout (the borrowout bit). Logic: Diff = A ^ B ^ Bin (XOR operation). Bout = (~A & B) | ((~A | B) & Bin) (borrow occurs
if A is less than B or needs a borrow). Both circuits follow simple XOR logic for the primary result
and AND-OR logic to determine carry or borrow conditions.

### PROGRAM:

module fulladdsub(a,b,cin,bin,sum,carry,difference,borrow);
input a,b,cin,bin;
output sum,carry,difference,borrow;
assign sum=a^b^cin;
assign carry=(a^b)&cin|a&b;
assign difference=a^b^bin;
assign borrow=~(a^b)&bin|(~a)&b;
endmodule

### TRUTH TABLE
![Screenshot 2024-11-28 141901](https://github.com/user-attachments/assets/92b6f83e-952d-4fe0-9c29-ca2f29857671)
![Screenshot 2024-11-28 141917](https://github.com/user-attachments/assets/2becd3db-b744-4806-a8d5-78da043c7733)

### RTL OUTPUT:
![Screenshot 2024-11-28 141941](https://github.com/user-attachments/assets/af3d292b-e4ae-47dd-98a1-5737f8d7c309)

### OUTPUT WAVEFORM:
![Screenshot 2024-11-28 141958](https://github.com/user-attachments/assets/abae107b-bbf7-45d7-877f-531f12bee1ea)

### RESULT:

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



