# Implementation-of-2-Input-NAND-Gate-using-CMOS-Technology
This repository presents the design of 2 Input NAND Gate . It is implemented on Synopsys Custom Compiler in 28nm technology node.
# Table of Contents
## Introduction
NAND gate is a logic gate which is
complement to AND gate. It is one of the two
universal gates. It is called universal gate as
we can implement any digital logic using
NAND gates.
The Boolean expression is
 F = (X.Y)’

Symbol –

Truth table of NAND Gate -
Case 1 – VA and VB are LOW.
As both are low the PUN will be ON and the
output will be changed to VDD as it gets two
paths through the PMOS to VDD. As PDN is
OFF there will be no connection between Vout
and GND as both NMOS are OFF.
Therefore, Vout is HIGH.
Case 2 -VA is LOW and VB is HIGH.PMOS1 – ON; PMOS2 – OFF; NMOS1 -OFF;
NMOS – ON; As we know in PUN the PMOS
are parallel the one which is ON establishes
connection between VDD and Output and as
NMOS are in series the PDN is still OFF
resulting Vout = HIGH.
Case 3- VA is HIGH and VB is LOW.
Similar to Case 2.
Case 4-VA is HIGH and VB is HIGH.
As both the PMOS in PUN are OFF there
won’t be any connection between VDD and Vout.
As the PDN is ON the Vout is connected GND.
Thus, Vout = LOW.
## Tools used
*Synopsys Custom Compiler*:  The Synopsys Custom Compiler™ design environment is a modern solution for full-custom analog, custom digital, and mixed-signal IC design. As the heart of the Synopsys Custom Design Platform, Custom Compiler provides design entry, simulation management and analysis, and custom layout editing features. This tool was used to design the circuit on a transistor level.<br/>
*Synopsys Primewave*:  PrimeWave™ Design Environment is a comprehensive and flexible environment for simulation setup and analysis of analog, RF, mixed-signal design, custom-digital and memory designs within the Synopsys Custom Design Platform. This tool helped in various types of simulations of the above designed circuit.<br/>
*Synopsys 28nm PDK*:  The Synopsys 28nm Process Design Kit(PDK) was used in creation and simulation of the above circuit design.<br/>

## NAND schematics
## NAND symbol
## Testbench schematics of 2 Input-NAND-Gate
## Simulation result

## Netlist
     *  Generated for: PrimeSim
*  Design library name: sm_nand
*  Design cell name: sm_nanddgn_tb
*  Design view name: schematic
.lib 'saed32nm.lib' TT

*Custom Compiler Version S-2021.09
*Tue Mar  1 10:38:15 2022

.global gnd!
********************************************************************************
* Library          : sm_nand
* Cell             : sm_nanddgn
* View             : schematic
* View Search List : hspice hspiceD schematic spice veriloga
* View Stop List   : hspice hspiceD
********************************************************************************
.subckt sm_nanddgn a b out vdc gnd_1
xm1 out b vdc vdc p105 w=0.1u l=0.03u nf=1 m=1
xm0 out a vdc vdc p105 w=0.1u l=0.03u nf=1 m=1
xm3 net13 b gnd_1 gnd_1 n105 w=0.1u l=0.03u nf=1 m=1
xm2 out a net13 net13 n105 w=0.1u l=0.03u nf=1 m=1
.ends sm_nanddgn

********************************************************************************
* Library          : sm_nand
* Cell             : sm_nanddgn_tb
* View             : schematic
* View Search List : hspice hspiceD schematic spice veriloga
* View Stop List   : hspice hspiceD
********************************************************************************
xi0 a b vout net7 gnd! sm_nanddgn
vdc net7 gnd! dc=1.8
v2 b gnd! dc=0 pulse ( 0 1.05 0 0.1u 0.1u 10u 20u )
v1 a gnd! dc=0 pulse ( 0 1.05 0 0.1u 0.1u 5u 10u )
c3 vout gnd! c=1p








.tran '1u' '20u' name=tran

.option primesim_remove_probe_prefix = 0
.probe v(*) i(*) level=1
.probe tran v(a) v(b) v(vout)

.temp 25



.option primesim_output=wdf


.option parhier = LOCAL






.end

## Author
N Nagamallishwar, Bachelor of Technology, Indian Institute of Information Technology, Tiruchirappalli
## Acknowledgements
* [Kunal Ghosh, Co-founder, VSD Corp. Pvt. Ltd.](https://www.linkedin.com/in/kunal-ghosh-vlsisystemdesign-com-28084836/)
* [Synopsys Inc](https://www.synopsys.com/)
* IIT Hyderabad
* Sameer Durgoji, NIT Karnataka
* Chinmaya Panda, IIT Hyderabad

## Reference
* [1] Digital Design,
Book by M. Morris Mano
* [2] Design of Analog CMOS Integrated Circuits -
McGraw Hill India
