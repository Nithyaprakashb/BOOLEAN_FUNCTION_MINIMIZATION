# BOOLEAN_FUNCTION_MINIMIZATION

**AIM:**

To implement the given logic function verify its operation in Quartus using Verilog programming.

F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D 

F2=xy’z+x’y’z+w’xy+wx’y+wxy

**Equipment Required:**

Hardware – PCs, Cyclone II , USB flasher

**Software – Quartus prime**

**Theory**

Boolean Function Minimization is the process of reducing a Boolean expression to its simplest form without changing its functionality. This minimization reduces the number of gates and inputs required, optimizing circuit design.

Logic Gates: Fundamental building blocks like AND, OR, and NOT gates are used to implement Boolean expressions. Karnaugh Map (K-map): A graphical technique for minimizing Boolean expressions by grouping terms based on commonalities. The given Boolean functions can be minimized as follows:

F1 = A’B’C’D’ + AC’D’ + B’CD’ + A’BCD + BC’D The terms can be simplified using K-map techniques to reduce the complexity of the circuit. F2 = xy’z + x’y’z + w’xy + wx’y + wxy Similar simplification can be done for this function to reduce the gate count. The resulting minimized expressions are implemented using Verilog HDL and simulated on the Quartus Prime tool. The outputs can then be verified on an FPGA board (e.g., Cyclone II).

**Logic Diagram**

![image](https://github.com/user-attachments/assets/b676919e-b80a-4acd-8f91-95b68e434cf1)

![image](https://github.com/user-attachments/assets/25b2145a-34ad-46d8-b0b0-fa17fff7f919)



**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**
~~~
/* Program to implement the given logic function and to verify its operations in quartus using Verilog programming. 

//Program to compute the function f1=a'b'c'd'+ac'd'+b'cd'+a'bcd+bc'd
//f2=xy'z+x'y'z+w'xy+wx'y+wxy
// simplify the logic using Boolean minimization/k map 
//compute f2 and write verilog code for f2 as like f1

module EX_02(a,b,c,d,w,x,y,z,f1,f2);
input a,b,c,d,w,x,y,z;
output f1,f2;
wire adash,bdash,cdash,ddash,ydash,p,q,r,s,t,u;
not(adash,a);
not(bdash,b);
not(cdash,c);
not(ddash,d);
not(ydash,y);
and(p,bdash,ddash);
and(q,adash,b,d);
and(r,a,b,cdash);
or(f1,p,q,r);

wire ybar,M,N,O;
not(ybar,y);
and(M,w,y);
and(N,x,y);
and(O,z,ybar);
or(f2,M,N,O);
endmodule
~~~

Developed by: NITHYA PRAKASH B
RegisterNumber: 212224050026


**RTL realization**

![image](https://github.com/user-attachments/assets/b52de6c8-39d3-4c08-a835-7137ef2d0283)


**Output:**

![image](https://github.com/user-attachments/assets/683cbc7e-89c5-43d4-973b-dbca1d7e1e0f)

**RTL**

**Timing Diagram**

![image](https://github.com/user-attachments/assets/a65673f7-a62c-4e5c-8df9-4120e6e2a281)


**Result:**

Thus the given logic functions are implemented using and their operations are verified using Verilog programming.

