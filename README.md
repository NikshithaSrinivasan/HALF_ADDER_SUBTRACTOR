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
```
Developed by: NIKSHITHA S
RegisterNumber: 24900161
```
```
Half adder:

module halfadder(a,b,sum,carry);
input a,b;
output sum,carry;
assign sum=a^b;
assign carry=a&b;
endmodule
```
```
Half subtractor:

module halfsubtractor(a,b,dif,borrow);
input a,b;
output dif,borrow;
assign dif=a^b;
assign borrow=~a&b;
endmodule
```
**RTL Schematic**
Half adder:
![halfadder circuit](https://github.com/user-attachments/assets/1d7066c8-e6bc-4e8f-b16b-044e012b954e)

Half subtractor:
![Screenshot 2024-12-03 181613](https://github.com/user-attachments/assets/18dcede4-a284-41c8-88ce-f1614e429d88)


**Output/TIMING Waveform**
Half adder:
![waveform halfadder](https://github.com/user-attachments/assets/b772117e-589b-4842-b9b3-2abe5951258e)

Half subtractor:
![Screenshot 2024-12-03 181445](https://github.com/user-attachments/assets/71921952-f77b-465f-91fe-a12508232fd1)

**Result:**
Thus, the Half Adder and Half Subtractor circuits are designed and the truth tables is verified using
 Quartus software.
