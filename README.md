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
```
module boolean_minimization(a,b,c,d,w,x,y,z,f1,f2);
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

and g1(s,ydash,z);
and g2(t,x,y);
and g3(u,w,z);
or g4(f2,s,t,u);
endmodule
```

# Developed by: PRASANNA I
# RegisterNumber:212223220079



# TRUTH TABLE
![Screenshot 2024-10-19 204015](https://github.com/user-attachments/assets/863d05a2-5423-4095-9d3f-2d086c5f07a4)

![Screenshot 2024-10-18 185600](https://github.com/user-attachments/assets/72b1be28-98eb-486f-9577-f3bc61a356be)

**RTL**


![Screenshot 2024-10-19 204037](https://github.com/user-attachments/assets/510f8e0f-4dfd-4395-8f87-dcf1cff2435e)

**Output:**


![Screenshot 2024-10-19 204053](https://github.com/user-attachments/assets/bddd246d-cb13-4f4c-99fc-6fb5515b9d8e)



**Result:**

Thus the given logic functions are implemented using and their operations are verified using Verilog programming.

