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

**FULL ADDER:**

![DE E-4 truthtable](https://github.com/04Varsha/FULL_ADDER_SUBTRACTOR/assets/149035374/7116d2bf-8e90-4e96-bfd5-d62af11a317a)

**FULL SUBTRACTOR:**

![DE E-4 subtractor truth table](https://github.com/04Varsha/FULL_ADDER_SUBTRACTOR/assets/149035374/33d8ba16-9169-40b0-8696-3bb8e5c3a0b7)


**Procedure**


**Full Adder:**
1. Open Quartus II and create a new project.
2. Use schematic design entry to draw the full adder circuit. 
3. The circuit consists of XOR, AND, and OR gates. 
4. Compile the design, verify its functionality through simulation. 
5. Implement the design on the target device and program it.

**Full Subtractor:** 
1. Follow the same steps as for the full adder. 
2. Draw the full subtractor circuit using schematic design. 
3. The circuit includes XOR, AND, OR gates to perform subtraction. 
4. Compile, simulate, implement, and program the design similarly to the full adder.


**Program:**

~~~
/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by: Aaron  I
RegisterNumber:212223230002
*/

## Full_adder
module proj_41(a,b,cin,sum,carry);
input a,b,cin;
output sum, carry;
assign sum=(a^b^cin);
assign carry=((a&b)|(b&cin)|(cin&a));
endmodule

## Full_subtractor
module proj_42(a,b,bin,borr,diff);
input a,b,bin;
output diff, borr;
assign diff=(a^b^bin);
assign borr=((~a&b)|(b&bin)|(bin&~a));
endmodule

~~~

**RTL Schematic**

**FULL ADDER**

![image](https://github.com/user-attachments/assets/b4f05a08-05de-4600-8f74-608be2fcd923)

**FULL SUBTRACTOR**

![image](https://github.com/user-attachments/assets/13bb6559-57ea-488e-a939-1d5b065c1cb6)

**Output Timing Waveform**

**FULL ADDER**

![image](https://github.com/user-attachments/assets/d49a074d-bf33-4198-922f-ac295f290ad4)

**FULL SUBTRACTOR**

![image](https://github.com/user-attachments/assets/fb9853a5-657d-4434-bf49-e7ef72331966)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



