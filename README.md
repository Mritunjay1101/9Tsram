# Table of Contents
            
* Introduction
* Devices Characteristics
* Circuit Design
* Simulation Results
* Conclusion
* Author
* Acknowledgements
* References

# Introduction
This repository contains details about the design and development of a 'Nine_Transistors' SRAM CELL under a hackathon organized by IIT Hyderabad and sponsored by Synopsys.
Here the tool used is Synopsys 'Custom-Compiler', which was used for schematics design and the  'Synopsis- Primewave' was is for the waveforms generation.
 
# Introduction
Any microprocessor requires high performance memory to access data exchange at very speeds, these memory units are designed with this SRAM technology, the fundamental bulilding block of such a memory unit is an SRAM cell.An SRAM (static random access memory) is a type of memory cell that is used to store one bit(0,1) of information, it fundamentally uses a latch(maade with MOSFETS) to store the information. Other type of memory that exists is a DRAM cell, which is made up of a capacitor and a MOSFET.But for high speed memory design former is considered.Both SRAM and DRAM are volatile memories. SRAM is more popular despite its high cost and low packing density as compared to DRAM because of its high speed, i.e., data can be read from the cell at a much faster rate.SRAM does not need periodic refreshing like the DRAM.

# Different Memories
2.1 Conventional 6T SRAM Cell
The conventional SRAM cell [1] made of 6 MOSFETs is the
most basic SRAM cell. Figure 1 shows the conventional 6T
SRAM cell schematic. This cell consists of two access
transistors and two cross-coupled inverters with a common
read and write port. Asserting a high value to WL enables the
access transistors for both read and write operations. For hold
operation, WL is set to a low value.
ADVANTAGES: This cell is simple in design and consumes
less area and thus can be used to design high-density memory
chips.
DISADVANTAGES: This cell fails to maintain its stability at
smaller-scaled technology. It suffers from read and write
instability, has high power consumption, and increased access
time when voltage scaling is done
2.2 4T SRAM Cell
The 6T SRAM cell although being the basic SRAM cell still
consumes more area as compared to the DRAM that has only
one transistor and one capacitor. So, to achieve a reduction in
area consumption by SRAM cell, a simpler design, i.e., 4T
SRAM cell was designed as shown in Figure 2. The 4T
SRAM consists of four NMOS and two poly-load resistors.
The PMOS transistors of the 6T cell are replaced by very high
polysilicon resistors to reduce transistor count and area
consumed by the cell [2].
ADVANTAGES: This cell comprises of lesser number of
transistors as well as consumes lesser area compared to the 6T
cell.
DISADVANTAGES: This cell is sensitive to noise and soft
error because of the very high resistances involved in the
design.7T SRAM cell [5] that has an additional
NMOS transistor N5 as compared to the conventional 6T
SRAM cell. The write operation in this cell depends on
removing the feedback connection between the two inverter
pairs before the write operation, and the transistor N5 serves
the purpose of feedback connection and disconnection. For
writing in this cell, N5 is turned OFF. During the read
operation, the cell behaves like a conventional 6T SRAM cell
with N5 in ON state.
ADVANTAGES: This cell has better cell operation, and
lower write power dissipation as compared to the
conventional SRAM cell.
DISADVANTAGES: Due to the additional transistor, the cell
area is 12.25% more than the 6T cell.
2.5 8T SRAM Cell
Figure 5 shows the circuit diagram of the 8T SRAM cell. This
cell consists of a separate circuit consisting of two additional
NMOS transistors for the read operation. This read circuit
provides a read mechanism that does not disturb the internal
nodes of the cell and thus improves the stability of the cell.
This cell has separate read and write word lines and
accommodates dual-port operation with separate read and
write bit lines [6].
ADVANTAGES: The 8T cell has better stability, higher
SNM, and lower power consumption. This cell also allows for
continued scaling compared to 6T cell that suffers from
various issues when scaled down.
DISADVANTAGES: The 8T cell consumes 30% more on the
chip as compared to the conventional 6T cell.
Figure 6 shows the schematic of a nine transistor SRAM cell.
This cell is designed with the aim of improving stability and
reducing power consumption. It can be viewed as a
combination of two sub-circuits – the upper and lower
sub-circuits. The upper sub-circuit is responsible for data
storage, and the lower sub-circuit contains transistors for bit
line access and read access. This cell uses a separate read
signal that controls the read access transistor N7 [7].
ADVANTAGES: This cell has 7.7% less leakage power and
also has better read stability as compared to the typical 6T
SRAM cell.
DISADVANTAGES: The area consumed by this cell is
37.8% more than the 6T cell, and the presence of three
stacked transistors in the read circuit increases the read access
time.
# Author
Mritunjay, BE(ECE), Panjab University, Chandigarh

# Acknowledgements
* [Kunal Ghosh, Co-founder, VSD Corp. Pvt Ltd.](#heading-1 "Goto https://www.linkedin.com/in/kunal-ghosh-vlsisystemdesign-com-28084836?lipi=urn%3Ali%3Apage%3Ad_flagship3_profile_view_base_contact_details%3B0xcWjpLDThSEo6S9UPO9Tw%3D%3D")
* Chinmaya Panda, IIT Hyderabad
* SumantoKAr
* Synopsys Team(Company)
* IIT Hyderabad
* Active and vibrant hackathon community
# References
1. Jan, M., Rabaey, Anantha Chandrakasan and Borivoje
Nikolic (2003),”Digital Integrated Circuits”, ISBN 81-
7808-991-2.
2. Agarwal, K. and Nassif, S. (2006), “Statistical Analysis of
SRAM Stability”, Proceedings of 43rd Annual Conference on
Design Automation, 57.
3. Design of Efficient Low Power Stable 4-Bit Memory Cell, K.
Gavaskar, Assistant professor/ECE, Kongu Engineering College,
Erode, India

