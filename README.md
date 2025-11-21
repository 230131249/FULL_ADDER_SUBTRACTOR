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

Full adder:

<img width="399" height="343" alt="image" src="https://github.com/user-attachments/assets/058fb54a-5a09-401b-b4a3-eb220472182f" />

Full subtractor:

<img width="433" height="337" alt="image" src="https://github.com/user-attachments/assets/7f798859-2dba-4c15-b1ba-b910ac90816f" />

**Procedure**
1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.

**Program:**

Full adder:

module ex6(a,b,c,sum,carry);

input a,b,c;

output sum,carry;

assign sum=(a^b^c);

assign carry=(a&b)|(b&c)|(c&a);

endmodule

Full subtractor:

module ex7(a,b,bin,d,bout);

input a,b,bin;

output d,bout;

assign d=(a^b^bin);

assign bout=(~a&bin)|(b&bin)|(~a&b);

endmodule


**RTL Schematic**

Full adder:

<img width="1920" height="1080" alt="Screenshot 2025-11-18 214751" src="https://github.com/user-attachments/assets/244d9351-b4eb-4af3-a783-3ffae98b8417" />

Full subtractor:

<img width="1920" height="1080" alt="Screenshot 2025-11-18 223909" src="https://github.com/user-attachments/assets/72780a24-0d84-4473-98ae-cf87f87002b2" />

**Output Timing Waveform**

Full adder:

<img width="1920" height="1080" alt="Screenshot 2025-11-18 215234" src="https://github.com/user-attachments/assets/35186705-39ee-4981-9b5f-e51f5c57a743" />

Full subtractor:

<img width="1920" height="1080" alt="Screenshot 2025-11-18 224103" src="https://github.com/user-attachments/assets/4951187e-617c-413c-bda7-49a8a8dba078" />


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



