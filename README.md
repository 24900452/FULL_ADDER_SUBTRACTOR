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

**Procedure**

Write the detailed procedure here

**Program:**
```
module ex4(sum,cout,a,b,cin);
output sum;
output cout;
input a;
input b;
input cin;
//Instantiate logic gate primitives
xor (sl,a,b);
and(cl,a,b);
xor(sum,sl,cin);
and(c2,sl,cin);
or(cout,c2,c1);
endmodule
```
```
module ex4a (df,bo,a,b,bin);
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

Developed by: RegisterNumber:24900452

**RTL Schematic**
![Screenshot (18)](https://github.com/user-attachments/assets/6223f995-2d3e-4a3c-bb83-336eec27df11)
![Screenshot (20)](https://github.com/user-attachments/assets/8e31ebb3-cb2c-4e5b-a4ee-4c5d972feb3e)

**Output Timing Waveform**
![Screenshot (19)](https://github.com/user-attachments/assets/a5bfcf9e-5e6f-49e2-a102-a5af0c5ec27f)
![Screenshot (21)](https://github.com/user-attachments/assets/e5bd8d27-c7a3-402e-aa00-6e04babd039a)

**Result:**


Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



