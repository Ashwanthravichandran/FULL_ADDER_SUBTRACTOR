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

![image](https://github.com/user-attachments/assets/ed756253-d944-431b-b915-a70b52ffba23)
![image](https://github.com/user-attachments/assets/cff5a53d-d8b9-42b2-b439-9de800274ddc)
![image](https://github.com/user-attachments/assets/7374934c-ab90-4084-8291-be936409fdeb)
![image](https://github.com/user-attachments/assets/0a7be7d1-734e-4a91-ac37-479e04eac189)


**Procedure**

Write the detailed procedure here

**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by:R Ashwanth RegisterNumber: 24900175
```
 module exp4(sum,cout,a,b,cin);
 output sum;
 output cout;
 input a;
 input b; 
 input cin;
 wire s1,c1,c2;
 xor(s1,a,b);
 and(c1,a,b);
 xor(sum,s1,cin);
 and(c2,s1,cin);
 or(cout,c2,c1);
 endmodule
```
```
module exp4b(df,bo,a,b,bin);
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
```

**RTL Schematic**  Full adder



![Screenshot 2024-11-16 084027](https://github.com/user-attachments/assets/986736ab-79c7-4d77-b141-a9d9348a0cb8)


Full subtractor


![Screenshot 2024-11-16 085113](https://github.com/user-attachments/assets/578e6e16-d870-4d7a-a78b-705811449912)

**Output Timing Waveform**

Full adder
![Screenshot 2024-11-16 084212](https://github.com/user-attachments/assets/54f4619d-3e50-407a-a15a-043f9e56152f)
Full subtractor
![Screenshot 2024-11-16 085223](https://github.com/user-attachments/assets/a324219d-ea54-4f1f-a518-7d27cb961782)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



