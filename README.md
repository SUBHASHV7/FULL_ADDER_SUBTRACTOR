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

**FULL ADDER**

![430851803-fdff1b53-0875-47ae-bc60-d4282f99efec](https://github.com/user-attachments/assets/e79038ea-4e44-4d04-8af3-353c7d9b2648)

**FULL SUBTRACTOR**

![430851983-028d8d6c-7dda-4ceb-b495-e837e3ae53b3](https://github.com/user-attachments/assets/f52a6de9-aa03-4986-a88d-43d6449399f6)

**Procedure**

*Full Adder*: 1.Open Quartus II and create a new project. 2.Use schematic design entry to draw the full adder circuit. 3.The circuit consists of XOR, AND, and OR gates. 4.Compile the design, verify its functionality through simulation. 5.Implement the design on the target device and program it.

*Full Subtractor*: 1.Follow the same steps as for the full adder. 2.Draw the full subtractor circuit using schematic design. 3.The circuit includes XOR, AND, OR gates to perform subtraction. 4.Compile, simulate, implement, and program the design similarly to the full adder.

**Program:**

Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. 

Developed by: SUBHASH V

RegisterNumber: 212224240163

~~~
//expt4a-full adder
module ex4a(sum, cout, a, b, cin);
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


//exp-4b-full subtractor
module ex4b(df, bo, a, b, bin);
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
~~~

**RTL Schematic**
**FULL ADDER**

![430853570-d009b821-53f6-4ef2-baf3-1c9f809febe7](https://github.com/user-attachments/assets/92479cbd-8675-476c-ae60-134efc7395bd)

**FULL SUBTRACTOR**

![430853752-9a44bd3e-145e-4035-ba3c-4f2bf94f4294](https://github.com/user-attachments/assets/ec764f25-2b5b-4c7b-9b1d-a401ad0fb293)

**Output Timing Waveform**
**FULL ADDER**

![430853863-d9d8a74d-6a47-4b1f-9d6b-d60f3353ff93](https://github.com/user-attachments/assets/5b8b0061-0e05-4cdd-8716-335644d0d045)

**FULL SUBTRACTOR**

![430854454-c74db76f-3c6f-44b8-a1e1-b33195f0832d](https://github.com/user-attachments/assets/a7b99ed6-4ae7-412a-8339-e5ee3bb387b6)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



