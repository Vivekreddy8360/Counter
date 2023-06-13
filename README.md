### Ex. No. 6
#### Date: 19.5.23
# Implementation of 4 bit synchronous counters using Verilog HDL
## Aim:
To design and implement the following synchronous counters using Verilog HDL.
1.	UP counter
2.	DOWN counter
## Components Required:
1.	Laptop with Quartus software and modelsim software.
## Theory:
A Synchronous counter is the counter in which the clock input with all the flip-flops uses the same source and produces the output at the same time.
## UP Counter
### State table
![image](https://github.com/rvinifa/Counter/assets/133735746/ede78598-89fd-4aeb-9d82-329e45d05f2a)

### K-map Simplification

   ![image](https://github.com/rvinifa/Counter/assets/133735746/21554263-611b-44a2-8f78-7b2220ef5a05)
   
### Logic Diagram
![image](https://github.com/rvinifa/Counter/assets/133735746/2ab715d3-f6d5-4cf6-8fda-8fa666518c0b)



## DOWN Counter
### State Table
 ![image](https://github.com/rvinifa/Counter/assets/133735746/5be9585c-11aa-47c3-beaf-0dca916750f2)

### K-map simplification
 ![image](https://github.com/rvinifa/Counter/assets/133735746/dde7bc60-3a4f-4fb7-811d-f420cb74bdef)

### Logic Diagram
 ![image](https://github.com/rvinifa/Counter/assets/133735746/64e2d7b7-1646-4ca7-bc6c-c7c10881223c)

## Procedure:
1.	Type the program in Quartus software.
2.	Compile and run the program.
3.	Generate the RTL schematic and save the logic diagram.
4.	Create nodes for inputs and outputs to generate the timing diagram.
5.	For different input combinations, generate the timing diagram.


## Program:
~~~
Developed by: M.vivek reddy
Reg No: 212221240030
~~~
## UP-COUNTER
```
module exp6(clk,q1,q2,q3,q4);
input clk;
output reg q1,q2,q3,q4;
always @(posedge clk)
begin
q4=(q1&q2&q3)^q4;
q3=(q1&q2)^q3;
q2=q1^q2;
q1=1^q1;
end
endmodule
```
## DOWN-COUNTER
```
module ex6b(clk,q1,q2,q3,q4);
input clk;
output reg q1,q2,q3,q4;
always@ (posedge clk)
begin
 q4=((~q1)&(~q2)&(~q3))^q4;
 q3=((~q1)&(~q2))^q3;
 q2=(~q1)^q2;
 q1=1^q1;
end
endmodule 
```
## RTL Schematic:
## UP-COUNTER
![image](https://github.com/Vivekreddy8360/Counter/assets/94525701/cf0684bb-e1a5-4a05-98d8-33372d028313)

## DOWN-COUNTER
![down](https://github.com/Vivekreddy8360/Counter/assets/94525701/de2c14ad-ebcc-496b-92c0-bc94a18c1902)

## Timing Diagram:
## UP-COUNTER
![up counter](https://github.com/Vivekreddy8360/Counter/assets/94525701/345376ae-2a22-41da-aa17-e0a935ddce23)
## DOWN-COUNTER
![downcounter](https://github.com/Vivekreddy8360/Counter/assets/94525701/4e0d2fed-773a-401d-9a7b-bac6ec914dab)

## Result:
Thus the Synchronous UP and DOWN counters using T flipflops are implemented and the state tables are verified.

