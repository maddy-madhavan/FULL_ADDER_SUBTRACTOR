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
FULL ADDER 
![Screenshot 2024-12-06 140823](https://github.com/user-attachments/assets/4de1482f-d6b1-4c10-9bdf-7228e650f397)
FULL SUBRACTOR
![Screenshot 2024-12-06 140958](https://github.com/user-attachments/assets/863c4134-d246-439b-a04f-06b3a663e85a)



**Truthtable**

**Procedure**

Write the detailed procedure here

**Program:**
FULL SUBRACTOR
module exp4(sum,cout,a,b,cin);
output sum;
outputput cout;
input a;
input b;
input cin;
//internal nets
wire s1,c1,c2;
//Instantiate logic gate primitives
xor(s1,a,b);
and(c1,a,b);
xor(sum,s1,cin);
and(c2,s1,cin);
or(cout,c2,c1);
endmodule
FULL ADDER
module exp5 (df,bo,a,b,bin);
output df;
output bo;
input a;
input b;
input bin;
wire w1,w2,w3;
assign w1=a^b;
assign w2=(~a&b);
assign w3=(~w1&bin); 
assign df=w1^bin;
assign bo=w2|w3;
endmodule
/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by: RegisterNumber:24901129
*/

**RTL Schematic**
\\\
FULL ADDER
![Screenshot 2024-12-06 135852](https://github.com/user-attachments/assets/914368dd-6f2e-467f-9f0e-92a475bb2369)
FULL SUBRACTOR
![Screenshot 2024-12-06 140111](https://github.com/user-attachments/assets/eb7e048c-bfdf-4d34-b636-96264135951b)


**Output Timing Waveform**
\\\
FULL ADDER 
![Screenshot 2024-12-06 140214](https://github.com/user-attachments/assets/2048ca75-34b6-4540-8ca1-32a66f3f52fc)
FULL SUBRACTOR
![Screenshot 2024-12-06 140346](https://github.com/user-attachments/assets/cdb7d95c-33e9-420d-9209-7b779d3feee2)




**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



