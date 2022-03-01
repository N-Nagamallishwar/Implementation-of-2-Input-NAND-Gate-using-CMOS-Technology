# Implementation-of-2-Input-NAND-Gate-using-CMOS-Technology<br/>
This repository presents the design of 2 Input NAND Gate . It is implemented on Synopsys Custom Compiler in 28nm technology node.<br/>
# Table of Contents<br/>
* [Introduction](https://github.com/N-Nagamallishwar/Implementation-of-2-Input-NAND-Gate-using-CMOS-Technology/edit/main/README.md##Introduction)<br/>
* [Tools used](https://github.com/N-Nagamallishwar/Implementation-of-2-Input-NAND-Gate-using-CMOS-Technology/edit/main/README.md##Tools-used)<br/>
* [NAND schematics](https://github.com/N-Nagamallishwar/Implementation-of-2-Input-NAND-Gate-using-CMOS-Technology/edit/main/README.md##NAND-schematics)<br/>
 * [NAND symbol](https://github.com/N-Nagamallishwar/Implementation-of-2-Input-NAND-Gate-using-CMOS-Technology/edit/main/README.md##NAND-symbol)<br/>
 * [NAND Testbench schematics](https://github.com/N-Nagamallishwar/Implementation-of-2-Input-NAND-Gate-using-CMOS-Technology/edit/main/README.md##NAND-Testbench-schematics)<br/>
 * [Simulation result](https://github.com/N-Nagamallishwar/Implementation-of-2-Input-NAND-Gate-using-CMOS-Technology/edit/main/README.md##Simulation-result)<br/>
 * [Netlist](https://github.com/N-Nagamallishwar/Implementation-of-2-Input-NAND-Gate-using-CMOS-Technology/edit/main/README.md##Netlist)<br/>
 * [Author](https://github.com/N-Nagamallishwar/Implementation-of-2-Input-NAND-Gate-using-CMOS-Technology/edit/main/README.md##Author)<br/>
 * [Acknowledgements](https://github.com/N-Nagamallishwar/Implementation-of-2-Input-NAND-Gate-using-CMOS-Technology/edit/main/README.md##Acknowledgements)<br/>
 * [Reference](https://github.com/N-Nagamallishwar/Implementation-of-2-Input-NAND-Gate-using-CMOS-Technology/edit/main/README.md##Reference)<br/>

## Introduction<br/>
NAND gate is a logic gate which is
complement to AND gate. It is one of the two
universal gates. It is called universal gate as
we can implement any digital logic using
NAND gates.<br/>
The Boolean expression is<br/>
 F = (X.Y)’<br/>

Symbol –<br/>

Truth table of NAND Gate -<br/>
Case 1 – VA and VB are LOW.<br/>
As both are low the PUN will be ON and the
output will be changed to VDD as it gets two
paths through the PMOS to VDD. As PDN is
OFF there will be no connection between Vout
and GND as both NMOS are OFF.<br/>
Therefore, Vout is HIGH.<br/>
Case 2 -VA is LOW and VB is HIGH.<br/>
PMOS1 – ON; PMOS2 – OFF;<br/> 
NMOS1 -OFF; NMOS – ON; <br/>
As we know in PUN the PMOS
are parallel the one which is ON establishes
connection between VDD and Output and as
NMOS are in series the PDN is still OFF
resulting Vout = HIGH.<br/>
Case 3- VA is HIGH and VB is LOW.<br/>
Similar to Case 2.<br/>
Case 4-VA is HIGH and VB is HIGH.<br/>
As both the PMOS in PUN are OFF there
won’t be any connection between VDD and Vout.
As the PDN is ON the Vout is connected GND.
Thus, Vout = LOW.<br/>
## Tools used<br/>
* Synopsys Custom Compiler:  The Synopsys Custom Compiler™ design environment is a modern solution for full-custom analog, custom digital, and mixed-signal IC design. As the heart of the Synopsys Custom Design Platform, Custom Compiler provides design entry, simulation management and analysis, and custom layout editing features. This tool was used to design the circuit on a transistor level.<br/>
* Synopsys Primewave:  PrimeWave™ Design Environment is a comprehensive and flexible environment for simulation setup and analysis of analog, RF, mixed-signal design, custom-digital and memory designs within the Synopsys Custom Design Platform. This tool helped in various types of simulations of the above designed circuit.<br/>
* Synopsys 28nm PDK:  The Synopsys 28nm Process Design Kit(PDK) was used in creation and simulation of the above circuit design.<br/>

## NAND schematics<br/>
## NAND symbol<br/>
## NAND Testbench schematics<br/>
## Simulation result<br/>

## Netlist<br/>
    
## Author<br/>
N Nagamallishwar, Bachelor of Technology, Indian Institute of Information Technology, Tiruchirappalli
## Acknowledgements<br/>
* [Kunal Ghosh, Co-founder, VSD Corp. Pvt. Ltd.](https://www.linkedin.com/in/kunal-ghosh-vlsisystemdesign-com-28084836/)<br/>
* [Synopsys Inc](https://www.synopsys.com/)<br/>
* IIT Hyderabad<br/>
* Sameer Durgoji, NIT Karnataka<br/>
* Chinmaya Panda, IIT Hyderabad<br/>

## Reference<br/>
* [1] Digital Design,
Book by M. Morris Mano
* [2] Design of Analog CMOS Integrated Circuits -
McGraw Hill India
