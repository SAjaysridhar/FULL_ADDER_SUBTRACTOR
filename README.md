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

Full adder

![Screenshot (22)](https://github.com/user-attachments/assets/dcd08949-2638-45a9-809f-57045959e3a8)


Full subtracter


![WhatsApp Image 2024-11-12 at 11 23 48_68934fab](https://github.com/user-attachments/assets/b1f3f487-235d-4972-bf07-5d7510629b6e)


**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.

**Program:**
```
//full adder
module ex4(sum, cout, a, b, cin);
output sum;
output cout;
input a;
input b; 
input cin;
//internal nets 
wire sl, cl,c2;
//Instantiate logic gate primitives 
xor (sl,a,b); 
and(cl,a,b);
xor(sum, sl, cin);
and(c2, sl, cin);
or (cout, c2,cl); 
endmodule
```
```
module ex4a (df, bo, a, b, bin);
 output df;
 output bo;
 input a;
 input b;
 input bin;
 wire w1,w2, w3;
 assign w1=a^b;
 assign w2=(~a&b); 
 assign w3=(~w1&bin);
 assign df=w1^bin;
 assign bo=w2|w3;
 endmodule
```
/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by:AJAY S  RegisterNumber:
24900457

**RTL Schematic**

Full adder
![WhatsApp Image 2024-11-12 at 11 04 48_ace2c709](https://github.com/user-attachments/assets/00e5f958-7a97-49af-a7c8-61e261b41c85)

Full subtracter
![WhatsApp Image 2024-11-12 at 11 06 51_3cedeb52](https://github.com/user-attachments/assets/fa38b733-784f-44b6-8db3-981b2501f9df)

**Output Timing Waveform**


Full adder 
![Screenshot (19)](https://github.com/user-attachments/assets/c4e0af58-13f6-474f-b3fd-7798aa260b8e)

Full subtracter
![Screenshot (21)](https://github.com/user-attachments/assets/504fdfcc-f1c8-4ab8-928c-4da02c0ce173)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



