# BOOLEAN_FUNCTION_MINIMIZATION

**AIM:**

To implement the given logic function verify its operation in Quartus using Verilog programming.

F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D 

F2=xy’z+x’y’z+w’xy+wx’y+wxy

**Equipment Required:**

Hardware – PCs, Cyclone II , USB flasher

**Software – Quartus prime**

**Theory**

**Logic Diagram**

**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**

**2A**
~~~
module ex2a(a,b,c,d,f1);
input a,b,c,d;
output f1;
assign f1=((~a&b&d)|(~b&~d)|(a&b&~c));
endmodule
~~~

**2B**
~~~
module ex2b(w,x,y,z,f2);
input w,x,y,z;
output f2;
assign f2=((~y&z)|(x&y)|(w&y));
endmodule
~~~

Developed by: NITHYA PRAKASH B
RegisterNumber: 212224050026


**RTL realization**

**2A**

![image](https://github.com/user-attachments/assets/83b4f25f-1657-4928-aad4-877cf9665a06)


**2B**

![image](https://github.com/user-attachments/assets/a314a609-5248-4894-a792-52f8a66acb3b)


**Output:**

**2A**

![image](https://github.com/user-attachments/assets/4627ec07-4607-4bd9-994e-521e97a47a96)


**2B**

![image](https://github.com/user-attachments/assets/84584f87-68b1-47a5-a7a9-5f1dd7fbf29a)

**RTL**

**2A**

![image](https://github.com/user-attachments/assets/27786186-9c58-44fb-a987-eb7a0939ab27)

**2B**

![image](https://github.com/user-attachments/assets/02525fd9-03f1-4334-86f5-585abfbf6c06)


**Result:**

Thus the given logic functions are implemented using and their operations are verified using Verilog programming.
