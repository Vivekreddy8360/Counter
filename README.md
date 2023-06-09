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
module UC(input CLK,input reset,output[0:3]counter);
reg[0:3]counter_up;
always@(posedge CLK or posedge reset)
begin 
if(reset)
counter_up<=4'd0;
else
counter_up<=counter_up+4'd1;
end
assign counter=counter_up;
endmodule
```
## DOWN-COUNTER
```
module DC(input CLK,input reset,output[0:3]counter);
reg[0:3]counter_down;
always@(posedge CLK or posedge reset)
begin 
if(reset)
counter_down<=4'd0;
else
counter_down<=counter_down-4'd1;
end
assign counter=counter_down;
endmodule
```
## RTL Schematic:
## UP-COUNTER
![image](https://github.com/Vivekreddy8360/Counter/assets/94525701/d2ce5054-f64c-4b61-a592-5047c70940b7)

## DOWN-COUNTER
![image](https://github.com/Vivekreddy8360/Counter/assets/94525701/98bd0a34-2818-46ca-9485-ecd44f93d847)

## Timing Diagram:
## UP-COUNTER
![image](https://github.com/Vivekreddy8360/Counter/assets/94525701/21461423-2ba3-4107-b987-d1c105be661d)
## DOWN-COUNTER
![image](https://github.com/Vivekreddy8360/Counter/assets/94525701/6776af1c-8901-4cef-9ff9-751c1e4e85b7)
## Result:
Thus the Synchronous UP and DOWN counters using T flipflops are implemented and the state tables are verified.

