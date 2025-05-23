# HALF_ADDER_SUBTRACTOR

Implementation-of-Half-Adder-and-Half Subtractor-circuit

**AIM:**

To design a half adder and half subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher 

Software – Quartus prime Theory Adders are digital circuits that carry out the addition of numbers.

**Half Adder**

Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

![image](https://github.com/naavaneetha/HALF_ADDER_SUBTRACTOR/assets/154305477/bd4a0b2c-cdbc-4184-ab08-81578f121e1f)

Figure -01 HALF ADDER

**Half Subtractor**

The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed. 

Diff = A’B+AB’ =A ⊕ B
Borrow = A’B

 ![image](https://github.com/naavaneetha/HALF_ADDER_SUBTRACTOR/assets/154305477/d76b099c-513f-4e7c-843a-e2fd028a531a)

Figure -02 HALF Subtractor

**Truthtable**

Half adder:

![Screenshot 2024-12-02 221545](https://github.com/user-attachments/assets/37372018-efad-4dd7-a437-927bfee50cdb)

Half subtractor:

![Screenshot 2024-12-02 221558](https://github.com/user-attachments/assets/82e07c7a-6002-4bd7-b470-1a6ede2ee3a3)

**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**
```python
Developed by: NIKSHITHA S
RegisterNumber: 212224040220
```
```python
module DE(a,b,sum,carry);
input a,b;
output sum,carry;
assign sum=(a^b);
assign carry=(a&b);
endmodule
module DE(x,y,diff,borr);
input x,y;
output diff,borr;
assign diff = (x^y);
assign borr = (~x&y);
endmodule
```
**RTL Schematic**
Half adder:

![image](https://github.com/user-attachments/assets/cb56901f-2cd3-4d6b-b742-9820425877c0)

Half subtractor:

![image](https://github.com/user-attachments/assets/239249bd-49fe-413c-93fb-6aa363b06bde)


**Output/TIMING Waveform**
Half adder:

![image](https://github.com/user-attachments/assets/3b4cbc4a-d731-4698-8e7a-26c9774aa967)

Half subtractor:

![Screenshot 2025-04-28 131936](https://github.com/user-attachments/assets/0c3b6417-d527-43a6-bdd7-92f061dcc791)


**Result:**
Thus, the Half Adder and Half Subtractor circuits are designed and the truth tables is verified using
 Quartus software.
