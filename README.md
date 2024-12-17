# D-FLIPDLOP-NEGEDGE

**AIM:**

To implement  D flipflop using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

A D flip-flop (also called a data flip-flop or delay flip-flop) is one of the most commonly used flip-flops in digital electronics. It captures the value of the data input 
D at a particular clock edge (rising or falling) and transfers it to the output 
Q. The output remains constant until the next clock edge.

**D Flip-Flop**

D flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, D latch operates with enable signal. That means, the output of D flip-flop is insensitive to the changes in the input, D except for active transition of the clock signal. The circuit diagram of D flip-flop is shown in the following figure.

![image](https://github.com/naavaneetha/D-FLIPDLOP-NEGEDGE/assets/154305477/48c81fe8-bc3f-40e7-95e2-519fc155ad51)

This circuit has single input D and two outputs Qtt & Qtt’. The operation of D flip-flop is similar to D Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable. The following table shows the state table of D flip-flop.

![image](https://github.com/naavaneetha/D-FLIPDLOP-NEGEDGE/assets/154305477/e5f3fda7-68ec-4a3a-a0a4-cf6f9cc4ab55)

Therefore, D flip-flop always Hold the information, which is available on data input, D of earlier positive transition of clock signal. From the above state table, we can directly write the next state equation as Qt+1t+1 = D

![image](https://github.com/naavaneetha/D-FLIPDLOP-NEGEDGE/assets/154305477/8592c0d8-2917-4142-91b9-d6c30dd891d2)

Next state of D flip-flop is always equal to data input, D for every positive transition of the clock signal. Hence, D flip-flops can be used in registers, shift registers and some of the counters.

**Procedure**

1. Type the program in Quartus software.

2. Compile and run the program.

3. Generate the RTL schematic and save the logic diagram.

4. Create nodes for inputs and outputs to generate the timing diagram.

5. For different input combinations generate the timing diagram.

**PROGRAM**

 Program for flipflops and verify its truth table in quartus using Verilog programming. 

**Developed by: Tauqir Ahmed S**

**RegisterNumber: 24013512**

module DFlipFlop(d, clk, rst, q, qbar);
 
 input d;
 
 input clk;
 
 input rst;
 
 output q;
 
 output qbar;

reg q;

reg qbar;

 always @ (posedge(clk) or posedge(rst)) begin
 
 if (rst==1'b1)

begin

q=1'b0;

qbar=1'b1;

end

else if (d==1'b0)

begin

q=1'b0;

qbar=1'b1;

end

else

begin

q=1'b1;

qbar=1'b0;

end 

end 

endmodule

**RTL LOGIC FOR FLIPFLOPS**

![Screenshot 2024-12-17 182929](https://github.com/user-attachments/assets/9e6aa201-a49a-42fb-a4af-3ca5f0202c2d)


**TIMING DIGRAMS FOR FLIP FLOPS**

![Screenshot 2024-12-17 183057](https://github.com/user-attachments/assets/be1cc22a-83f8-4f86-9969-e5972a08b197)


**RESULTS**

The D flip-flop was implemented successfully using Verilog, and its functionality was validated through simulation. The output matches the expected functional table of the D flip-flop.
