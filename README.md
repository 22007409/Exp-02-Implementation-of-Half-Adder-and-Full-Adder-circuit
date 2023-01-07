Developed by:V Sandhiya 

RegisterNumber:22007409  

AIM:
To design a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming.

Equipments Required:
Hardware – PCs, 

           Cyclone II ,
           
           USB flasher
           
Software – Quartus prime
           Theory Adders are digital circuits that carry out addition of numbers.

Half Adder

Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B
Carry = AB

Full Adder

Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin
Carry = AB + ACin + BCin

Figure -01 HALF ADDER 

![INIYA 1](https://user-images.githubusercontent.com/121559414/211154010-7a791c1f-76a8-4854-94c3-44d9b9887c7a.png)

Figure -02 FULL ADDER 

![INIYA 2](https://user-images.githubusercontent.com/121559414/211154146-c7360e1c-bacf-482a-8714-367767c3076a.png)

Procedure

Connect the supply (+5V) to the circuit Switch ON the main switch If the output is 1, then the led glows.

Program:

Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.

HALF ADDER  

module HalfAdder(a,b,sum,carry);
input a,b;
output sum,carry;
xor(sum,a,b);
and(carry,a,b);
endmodule  

FULL ADDER  

module FullAdder(a,b,c,sum,carry);
input a,b,c;
output sum,carry;
assign sum = ((a^b)^c);
assign carry = ((a&b)|(b&c)|(c&a));
endmodule  


Logic symbol
![INIYA 3](https://user-images.githubusercontent.com/121559414/211154323-908bd6ee-23f2-4153-8c33-6102904a6a35.png)

Output:
RTL realization

HALF ADDER

![INIYA 4](https://user-images.githubusercontent.com/121559414/211154399-56f23940-6efb-4f17-b750-8ec6d5db313c.png)

FULL ADDER

![INIYA 5](https://user-images.githubusercontent.com/121559414/211154425-a2c0cec9-cd30-4f24-9661-1995e7c992d5.png)

TIMING DIAGRAM

HALF ADDER

![INIYA 6](https://user-images.githubusercontent.com/121559414/211154483-7bc36a1d-c50b-4155-8b77-ecf08dd7d389.png)

FULL ADDER

![INIYA 7](https://user-images.githubusercontent.com/121559414/211154508-c55e3376-0511-4f2c-be55-2b3947651d56.png)

TRUTH TABLE

HALF ADDER

![INIYA 8](https://user-images.githubusercontent.com/121559414/211154541-6c702955-b220-4485-9b0c-c6f9eed71595.png)

FULL ADDER

![INIYA 9](https://user-images.githubusercontent.com/121559414/211154562-1aad4026-8bec-48ac-9e1a-fde2a4060426.png)

Result:
Thus the Implementation of Half Adder and Full Adder circuit are studied and the truth table for different logic gates are verified.

