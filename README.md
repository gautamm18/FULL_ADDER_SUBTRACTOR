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

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
 Developed by: GAUTAM P
 RegisterNumber: 212225230073*/
Full adder
```
module exp4(sum, carry, a, b, cin);
    output sum;
    output carry;
    input a;
    input b;
    input cin;

    assign sum = a ^ b ^ cin;
    assign carry = (a & b) | (cin & (a ^ b));
endmodule
```
Full subtractor
```
module exp42(diff, borrow, a, b, bin);
    output diff;
    output borrow;
    input a;
    input b;
    input bin;

    assign diff = a ^ b ^ bin;
    assign borrow = (a & b) | ((a ^ b) & bin);
endmodule
```
**RTL Schematic**
FULL ADDER
<img width="816" height="334" alt="image" src="https://github.com/user-attachments/assets/b7dc6abd-3ce5-45db-b29a-c0c9868f38af" />

FULL SUBTRACTOR
<img width="1095" height="425" alt="image" src="https://github.com/user-attachments/assets/2caddb06-fe84-42f6-b752-65a915aad116" />

**Output Timing Waveform**
FULL ADDER
<img width="1876" height="457" alt="image" src="https://github.com/user-attachments/assets/4f801829-2b20-49b3-8eee-ed63f47e9a0c" />

FULL SUBTRACTOR
<img width="1365" height="476" alt="Screenshot 2026-05-24 211243" src="https://github.com/user-attachments/assets/35257368-71b2-4a30-b885-cd96cf06c45b" />

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



