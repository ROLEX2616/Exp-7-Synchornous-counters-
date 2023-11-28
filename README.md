# Exp-6-Synchornous-counters - up counter and down counter 
### AIM: To implement 4 bit up and down counters and validate  functionality.
### HARDWARE REQUIRED:  – PC, Cyclone II , USB flasher
### SOFTWARE REQUIRED:   Quartus prime
### THEORY 

## UP COUNTER 
The counter is a digital sequential circuit and here it is a 4 bit counter, which simply means it can count from 0 to 15 and vice versa based upon the direction of counting (up/down). 

The counter (“count“) value will be evaluated at every positive (rising) edge of the clock (“clk“) cycle.
The Counter will be set to Zero when “reset” input is at logic high.
The counter will be loaded with “data” input when the “load” signal is at logic high. Otherwise, it will count up or down.
The counter will count up when the “up_down” signal is logic high, otherwise count down

Since we know that binary count sequences follow a pattern of octave (factor of 2) frequency division, and that J-K flip-flop multivibrators set up for the “toggle” mode are capable of performing this type of frequency division, we can envision a circuit made up of several J-K flip-flops, cascaded to produce four bits of output.
The main problem facing us is to determine how to connect these flip-flops together so that they toggle at the right times to produce the proper binary sequence.
Examine the following binary count sequence, paying attention to patterns preceding the “toggling” of a bit between 0 and 1:
Binary count sequence, paying attention to patterns preceding the “toggling” of a bit between 0 and 1.

Note that each bit in this four-bit sequence toggles when the bit before it (the bit having a lesser significance, or place-weight), toggles in a particular direction: from 1 to 0.



 
 

Starting with four J-K flip-flops connected in such a way to always be in the “toggle” mode, we need to determine how to connect the clock inputs in such a way so that each succeeding bit toggles when the bit before it transitions from 1 to 0.

The Q outputs of each flip-flop will serve as the respective binary bits of the final, four-bit count:

 
 

Four-bit “Up” Counter
![image](https://user-images.githubusercontent.com/36288975/169644758-b2f4339d-9532-40c5-af40-8f4f8c942e2c.png)



## DOWN COUNTER 

As well as counting “up” from zero and increasing or incrementing to some preset value, it is sometimes necessary to count “down” from a predetermined value to zero allowing us to produce an output that activates when the zero count or some other pre-set value is reached.

This type of counter is normally referred to as a Down Counter, (CTD). In a binary or BCD down counter, the count decreases by one for each external clock pulse from some preset value. Special dual purpose IC’s such as the TTL 74LS193 or CMOS CD4510 are 4-bit binary Up or Down counters which have an additional input pin to select either the up or down count mode.
![image](https://user-images.githubusercontent.com/36288975/169644844-1a14e123-7228-4ed8-81a9-eb937dff4ac8.png)


4-bit Count Down Counter
### Procedure

1.	Create a New Project:
Open Quartus and create a new project by selecting "File" > "New Project Wizard."
Follow the wizard's instructions to set up your project, including specifying the project name, location, and target device (FPGA).
2.	Create a New Design File:

Once the project is created, right-click on the project name in the Project Navigator and select "Add New File."
Choose "Verilog HDL File" or "VHDL File," depending on your chosen hardware description language.
3.	Write the Combinational Logic Code:

Open the newly created Verilog or VHDL file and write the code for your combinational logic.
4.	Compile the Project:
To compile the project, click on "Processing" > "Start Compilation" in the menu.
Quartus will analyze your code, synthesize it into a netlist, and perform optimizations based on your target FPGA device.
5.	Analyze and Fix Errors:

If there are any errors or warnings during the compilation process, Quartus will display them in the Messages window.
Review and fix any issues in your code if necessary.
View the RTL diagram.
6.	Verification:
Click on "File" > "New" > "Verification/Debugging Files" > "University Program VWF".
Once Waveform is created Right Click on the Input/Output Panel > " Insert Node or Bus" > Click on Node Finder > Click On "List" > Select All.
 
Give the Input Combinations according to the Truth Table amd then simulate the Output Waveform.




### PROGRAM 

![image](https://github.com/ROLEX2616/Exp-7-Synchornous-counters-/assets/149988469/e153c0b4-80ad-4bb2-ada7-a9af9cd555ff)

Program for flipflops  and verify its truth table in quartus using Verilog programming.
Developed by:Kavinraj.S
RegisterNumber:23011639
*/






### RTL LOGIC UP COUNTER AND DOWN COUNTER  


Down Counter 
![image](https://github.com/ROLEX2616/Exp-7-Synchornous-counters-/assets/149988469/4e131073-f05b-4b3f-a664-c749c16a46b8)




Up Counter
![image](https://github.com/ROLEX2616/Exp-7-Synchornous-counters-/assets/149988469/6536d62a-2a12-4340-9d1b-9c111c06fbfb)










### TIMING DIGRAMS FOR COUNTER  

Down Counter


![image](https://github.com/ROLEX2616/Exp-7-Synchornous-counters-/assets/149988469/633d9ad1-e3aa-4cdf-944f-dd710d8d6304)



UP Counter

![image](https://github.com/ROLEX2616/Exp-7-Synchornous-counters-/assets/149988469/832dff0b-73b8-4466-8491-60f8d3f3f8e4)







### TRUTH TABLE
 Down Counter and Up Counter

 ![image](https://github.com/ROLEX2616/Exp-7-Synchornous-counters-/assets/149988469/ab2bce08-6de2-42f0-846c-db6c1f019268)






## RESULT:
By this we have verified the truth table of 4-bit up-counter using verilog.








### RESULTS 
