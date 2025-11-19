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
FULLADDER
<img width="1167" height="663" alt="image" src="https://github.com/user-attachments/assets/aae8ee01-33a0-464a-9736-80e44f0cb907" />
FULLSUBTRACTOR
<img width="1140" height="673" alt="image" src="https://github.com/user-attachments/assets/807a66d4-5e61-43e8-9e12-a83a2977e293" />

**Procedure**

Write the detailed procedure here

**Program:**
```
FULLADDER

input a,b,cin;
output sum,carry;
assign sum=( (a ^ b)^cin);
assign carry= ( (a & b)| ( cin &(a ^ b )));
endmodule

FULLSUBTRACTOR

input a,b,bin;
output difference,borrow;
assign difference= ( (a ^ b)^bin);
assign borrow= ( ( ~a & b)| ( bin & (~(a ^ b ))));
endmodule
```
/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by: Deepika A  RegisterNumber:25018166
*/

**RTL Schematic**
FULLADDER
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/a6313326-1c9f-446e-a505-38b8196fb339" />
FULLSUBTRACTOR
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/f558575c-6cf7-4b05-ac14-e7089998eb16" />

**Output Timing Waveform**
FULLADDER
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/e46a2d4a-c8f1-4740-8de8-2c8e02b7fb4e" />
FULLSUBTRACTOR
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/a7aace2e-46b3-4787-a94f-467c876fcd75" />

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



