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
![Screenshot 2024-12-25 111327](https://github.com/user-attachments/assets/93015fc2-a4d2-4f9a-a173-8b264060bc1f)


![Screenshot 2024-12-25 111512](https://github.com/user-attachments/assets/053e6b53-1815-4e20-ba91-39673ef2293e)

**Procedure**


1.Type the program in Quartus software .


2.Compile and run the program .


3.Generate the RTL schematic and save the logic diagram.


4.create nodes for inputs and outputs to generate the timing diagram .


5.for different input combinations generate the timing diagram.

**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. 

Developed by: SWETHA S V RegisterNumber: 24000297
*/
```
*Full adder*
 module de4(a,b,c,sum,carry);
 input a,b,c;
 output sum,carry;
 xor(sum,a,b,c);
 assign carry=a&b | b&c | a&c;
 endmodule

*Full subractor*
module de42(diff,carry,a,b,c);
input a,b,c;
output diff,carry;
xor(diff,a,b,c);
assign carry= (~a)&c | (~a)&b | (b&c);
endmodule
```
**RTL Schematic**
![Screenshot 2024-12-25 111740](https://github.com/user-attachments/assets/70efdcc2-4da1-4300-b0f3-db6ed115846f)
![Screenshot 2024-12-25 111838](https://github.com/user-attachments/assets/a38dda8a-5b9f-4649-81d8-c831189cdcb3)

**Output Timing Waveform**
![Screenshot 2024-12-25 120953](https://github.com/user-attachments/assets/db88f9ef-cd97-45eb-8f2c-09391c3e3d49)
![Screenshot 2024-12-25 121138](https://github.com/user-attachments/assets/95de84f7-b730-491f-8a4e-e16efd50cb90)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



