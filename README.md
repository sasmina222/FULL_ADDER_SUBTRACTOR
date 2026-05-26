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

Full Adder

<img width="526" height="625" alt="image" src="https://github.com/user-attachments/assets/d455a3ae-2e65-453f-8bf6-2a05f67f5159" />

Full Subtractor

<img width="697" height="667" alt="image" src="https://github.com/user-attachments/assets/63afad4d-cd9a-4b54-8a54-fd2972f6f2ad" />



**Procedure**

Open the Verilog HDL software and create a new module for Full Adder and Full Subtractor.
Declare the inputs a, b, cin and outputs sum, carry, DIFF, BO.
Write the dataflow equations using assign statements for adder and subtractor outputs.
Compile the Verilog code and remove any syntax errors if present.
Simulate the program using a testbench and verify the outputs with the truth table.


**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.

Developed by:SASMINA S 

RegisterNumber:212225230254
*/
~~~
module exp3(a,b,cin,sum,carry,diff,borrow);
input a,b,cin;
output sum,carry,diff,borrow;
wire adash;
not (adash,a);
assign sum = a^b^cin;
assign carry = (a&b)|(b&cin)|(a&cin);
assign diff = a^b^cin;
assign borrow = (adash&b)|(b&cin)|(adash&cin);
endmodule 
~~~
**RTL Schematic**


<img width="1918" height="1021" alt="image" src="https://github.com/user-attachments/assets/aec2e3c7-2342-4259-862b-56866b59d544" />


**Output Timing Waveform**
<img width="1780" height="467" alt="image" src="https://github.com/user-attachments/assets/422b55da-c64d-4f9f-96e3-2cbf236a02c7" />


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



