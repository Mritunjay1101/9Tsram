# 9Tsram
##This repository contains details about the design and development of a 'Nine_Transistors' SRAM CELL under a hackathon organized by IIT Hyderabad along with Synopsys.
##Here the tool used is Synopsys Custom Compiler.
#Introduction
SRAM (static random access memory) is a type of
semiconductor random access memory that uses latches or
flip-flops to store data, and the data in it is stored indefinitely
provided the power is applied continuously. The other type of
random access memory is the DRAM (dynamic random
access memory), also a semiconductor MOS memory, that
uses a capacitor and a transistor to store data. Both SRAM
and DRAM are volatile memories. SRAM is more popular
despite its high cost and low packing density as compared to
DRAM because of its high speed, i.e., data can be read from
the cell at a much faster rate from SRAM compared to
DRAM. Also, SRAM does not need periodic refreshing like
the DRAM. Thus, SRAM is a choice for designers in
applications where high speed is a must, and the high cost of
the cell is tolerable as in the case of cache memory designing.
In the present time, where portable battery-operated devices
have become very common, power dissipation and area have
become major concerns leading to the demand for small and
low power consuming devices. Day by day, the scale of
integration is increasing to meet the small-sized and
high-density chips. This technology scaling results in
instability in SRAM cell operations. Conventional SRAM cell
suffers from various problems at smaller-scaled technology
like leakage current, read stability, etc. To achieve a design
that can work at smaller-scaled technology, various SRAM
cells have been developed. Since there exists a trade-off
between different parameters of an SRAM cell, so achieving
all the aspects in a single design is not possible. Therefore,
different designs depending upon different requirements in
different applications are developed by focusing on the
optimization of one or more parameters. This paper discusses
various SRAM cells that consist of a different number of
transistors and have some improved factors as compared to
one another and the advantages and disadvantages of
different SRAM cells are also seen.
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
