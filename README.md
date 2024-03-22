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

![315064567-e5e9b28c-8569-4f22-8d9a-f00f3791d592](https://github.com/23013633/FULL_ADDER_SUBTRACTOR/assets/150005961/cb984899-e6e5-40eb-82e2-f7023136f628)

Full Subtractor

![315065119-a549746d-5b01-4493-af45-09d21f7b1b39](https://github.com/23013633/FULL_ADDER_SUBTRACTOR/assets/150005961/4e0b884c-1d79-4803-94a6-10ddbbf44352)


**Procedure**

Write the detailed procedure here

**Program:**

```
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by: Thajesh K
RegisterNumber: 212223230229

module Fulladdsub(a,b,cin,sum,carry,BO,DIFF);
input a,b,cin;
output sum,carry,BO,DIFF;
assign sum=(a^b^cin);
assign carry=(a&b)|(a&cin)|(b&cin);
assign DIFF=(a^b^cin);
assign BO=(~a&b)|(~(a^b)& cin);
endmodule
```
**RTL Schematic**

![313991378-80d06b2e-6dbd-4f67-bf6b-d99f13b77d0c](https://github.com/23013633/FULL_ADDER_SUBTRACTOR/assets/150005961/5ba20fc4-4a11-40f3-9749-ce81e724d3df)

**Output Timing Waveform**

![313991290-0cc2e5bb-12b2-4593-a282-e444ee12875f](https://github.com/23013633/FULL_ADDER_SUBTRACTOR/assets/150005961/f087621a-eada-4b65-8082-6e512bd7b5b9)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.


