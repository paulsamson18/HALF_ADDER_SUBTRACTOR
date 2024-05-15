# Implementation-of-Half-Adder-and-Half Subtractor-circuit

Developed By :Paulsamson

Register Number : 212222230104

**AIM:**

To design a half adder and half subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher 

Software – Quartus prime Theory Adders are digital circuits that carry out the addition of numbers.

**Half Adder**

Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

![image](https://github.com/Nishanth-018/HALF_ADDER_SUBTRACTOR/assets/149347651/30e1e09b-4d6e-4f7a-9441-ae086bff0e58)

Figure -01 HALF ADDER

**Half Subtractor**

The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed. 

Diff = A’B+AB’ =A ⊕ B
Borrow = A’B

![image](https://github.com/Nishanth-018/HALF_ADDER_SUBTRACTOR/assets/149347651/aec377c7-f2c6-4134-9669-83e490c48f92)

Figure -02 HALF Subtractor

**Truthtable**

**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**

*Half_adder*
```
module halfadd_top(a,b,sum,carry);
input a,b;
output sum,carry; 
 assign sum = a^b;
 assign carry = a & b;
endmodule
```
*Half_subtractor*
```
module halfsub_top(a,b,D,Bo);
input a,b;
output D,Bo; // Outputs sum and carry for half adder:Outputs difference D,Borrow Bo for half subtractor
assign D = a ^ b;
  assign Bo = ~a & b;
endmodule
```
```
Developed by:paulsamson

RegisterNumber:212222230104

*/
```
**RTL Schematic**

![image](https://github.com/Nishanth-018/HALF_ADDER_SUBTRACTOR/assets/149347651/7b58e8ce-c1d0-4d1b-8912-cdf1a10e5556)

**Output/TIMING Waveform**

HALF ADDER:

![image](https://github.com/Nishanth-018/HALF_ADDER_SUBTRACTOR/assets/149347651/306ecaf0-8cfe-453e-9060-72bea621f1d7)

HALF SUBTRACTOR:

![image](https://github.com/Nishanth-018/HALF_ADDER_SUBTRACTOR/assets/149347651/eed28451-15c5-4184-97a0-c5691a04cb71)

**Result:**

Thus a  a half adder and half subtractor circuit is designed and its truth table in Quartus using Verilog programming is verified.
