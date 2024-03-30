ECTE 432 Project 2: MIPS PIPELINE 

Done by:
Edwin Dsouza
6279570
GitHub Link: ed722uowd/432-project-2 (github.com)
Contents
Simulink Circuit:	2
Waveforms:	2
First Branch:	7
Last High of Mem Write:	7
The use of multiple delays for testing:	8

 
Simulink Circuit:
 
Figure 1. MIPS Pipeline Structure
Waveforms:
Waveforms in increments of 32 clock cycles.
 
Figure 2. Overall Waveform
 
Figure 3. Clock Cycle 0 - 32
 
Figure 4. Clock Cycle 32 - 64
 
Figure 5. Clock Cycle 64 -96
 
Figure 6. Clock Cycle 96 -128
 
Figure 7. Clock Cycle 128 - 160
 
Figure 8. Clock Cycle 128 - 192
 
Figure 9 Clock Cycle 192 - 224
 
Figure 10. Clock Cycle 220 -250
First Branch:
 
Figure 11. First Branch
The waveform branches to the 8th instruction at the 44th clock cycle
Last High of Mem Write:
 
Figure 12. Last Mem Write high and Write data to data memory
Last high of Mem Write happens at the 156th clock cycle with the data written to memory being 30.
The use of multiple delays for testing:
The waveform for a particular output wouldn’t come when taken after a buffer (comprised of delay and register block). In order to deal with this, it was decided to use a delay block to delay the output till the Mem Stage. For instance, the PC counter had issues when trying to add it to the waveform viewer when taken from the EXE stage. To align the PC at the MEM stage a delay of 6 clock cycles was added to the PC at the fetch stage, since it had to traverse through 3 buffers each with a delay count of 2.
To confirm the working of the model, all waveforms were analyzed in the MEM stage using delay units in some cases.
