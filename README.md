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

FULL ADDER:
![image](https://github.com/user-attachments/assets/be10353a-5c70-4452-8a94-fa43a7cbd464)

FULL SUBTRACTOR:
![image](https://github.com/user-attachments/assets/4eeea00a-96ed-4891-8f7a-802147fc182e)


**Procedure**

Full Adder: 1.Open Quartus II and create a new project. 2.Use schematic design entry to draw the full adder circuit. 3.The circuit consists of XOR, AND, and OR gates. 4.Compile the design, verify its functionality through simulation. 5.Implement the design on the target device and program it.

Full Subtractor: 1.Follow the same steps as for the full adder. 2.Draw the full subtractor circuit using schematic design. 3.The circuit includes XOR, AND, OR gates to perform subtraction. 4.Compile, simulate, implement, and program the design similarly to the full adder.

**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by:MANIYARASAN R RegisterNumber:212224040185
```

     FULL-ADDER
module exp4add(sum, cout, a, b, cin);
output sum;
output cout;
input a;
input b;
input cin;
wire w1,w2,w3;
assign w1=a^b;
assign w2=a&b;
assign w3=w1&cin;
assign sum=w1^cin;
assign cout=w2|w3;
endmodule

       FULL SUBTRACTOR
module exp4sub(df, bo, a, b, bin);
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

**RTL Schematic**

![de4](https://github.com/user-attachments/assets/b8731eb0-de48-4ba4-8f35-8fc8b47d5012)
![de44](https://github.com/user-attachments/assets/d7e7e334-83d5-4eb7-9e4d-4e03f81b99d9)

**Output Timing Waveform**
![de444](https://github.com/user-attachments/assets/a21ac74d-6504-44b9-95a5-04843aa86e44)
![de4444](https://github.com/user-attachments/assets/9b6fd08d-5a3e-4176-96a7-8a437e032992)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



