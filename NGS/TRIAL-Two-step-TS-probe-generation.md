Optimization of probe generation for TEQUILA-SEQ
================================================================================
Description: Find optimal time conditions for new TS probesets

Materials:
--------------------------------------------------------------------------------
  * 10 ng/µl of TS probe template pool <br/> _Templates should end in sequence complementary to RC and not include Nt.BspQI sites._
  * 10 µM TEQUILA-SEQ universal reverse complement oligo([ARL1050](../ARL-primers.csv))
  * 10 mM dNTP mix (each nucleotide at 10 mM)
  * **10X NEBuffer 3.1 (~pH 7.9 at RT, included with nickase enzyme)**
    * 500 mM Tris-HCl
    * 1 M NaCl
    * 100 mM MgCl<sub/>2<sub>
    * 100 µg/ml BSA
  * 100 mM DTT
  * 10 mg/ml (~298 µM) [T4 Gene 32 Protein](https://www.neb.com/en-us/products/m0300-t4-gene-32-protein) (single standed DNA binding protein)
  * 5 units/µl (~14.7 µM) [Klenow Fragment (3´→5´ exo-)](https://www.neb.com/en-us/products/m0212-klenow-fragment-3-5-exo)
  * 10 units/µl [Nt.BspQI nickase](https://www.neb.com/en-us/products/r0644-ntbspqi)
  * 30 U/ul [Recj 5´-3´ DNA exonuclease](https://www.neb.com/en-us/products/m0264-recjf)
  * [SPRI beads](./SPRI-beads.md)
  * [High Sensitivity DNA TapeStation Reagents](https://www.agilent.com/en/product/automated-electrophoresis/tapestation-systems/tapestation-dna-screentape-reagents/high-sensitivity-dna-screentape-analysis-228262)
  
Equipment Required:
--------------------------------------------------------------------------------
  * Thermocycler
  * Magnetic stand
  * TapeStation

<br/><br/><br/><br/>

Protocol:
--------------------------------------------------------------------------------
### Day 1: Probe generation

### Template-RC annealing (~30 minutes)

**1.** Combine the following components on ice in the indicated order (add buffer last).

  | Component | [Stock] | Quantity | 
  | ---------: | :---------: |:---------- |
  | template pool | 10 ng/µl | **4**  µL | 
  | RC oligo | 2 µM | **5**  µL |
  | dNTP mix | 1 mM each | **3**  µL |
  | RNase-free water|| **14.2**  µL |
  | NEB Buffer 3.1| 10X | **3**  µL |
  | **Total** || **29.2** µL |
  <br/>
  
**2.** Anneal RC oligo to template pool in a thermocycler with the following program:  

  | Temp | Time | Step |
  | :--------: | :---------: |:---------: |
  | **95 °C** | **2:00** | **inital denaturation** |
  | **down to 4 °C** | **0.1 °C/sec** | **gradual ramp down** |
  | **4 °C** || **hold until next step** |
  
  _Note: Should take 15 minutes to ramp down from 95 to 4,_ <br/> _set Proflex ramp rate to 0.3 °C/sec to achieve this._
<br/>

<br/><br/><br/><br/>

### Intial extension and purification (~40 minutes)

**3.** To each sample, add the following components: <br/> _Tip: can spot 1 µL at tube tops and spin down to mix_

  | Component | [Stock] | Quantity | 
  | ---------: | :---------: |:---------- |
  | annealed mix || **29.2**  µL | 
  | DTT | 100 mM | **0.6**  µL |
  | Klenow Fragment| 5 U/µL | **0.2**  µL |
  | **Total** || **30** µL |
  <br/>

**4.** Incubate extension in a thermocycler for 15 minutes at 37 °C (set lid to 55 °C)

**5.** Add 0.2 µL (6 U) of RecJ and incubate for another 15 minutes at 37 °C

**6.** Clean up reaction products with 1.4X SPRI beads and 2 80 % ethanol washes. <br/> Elute products in 16 µL of water. Confirm by qubit and Tape.

### Isothermal strand displacement amplification (up to 2.5 hours)

**7.** **Dilute Nt.BspQI 5-fold** in water and, for each sample, combine the following components:

  | Component | [Stock] | Quantity | 
  | ---------: | :---------: |:---------- |
  | purified dsDNA template || **10**  µL | 
  | RNase-free water|| **7**  µL |
  | NEB Buffer 3.1 | 10X | **2**  µL |
  | Nt.BspQI | **2 U/µL** | **1**  µL |
  | **Total** || **20** µL | 
  <br/>

**8.** Incubate pre-nicking reaction at 50 °C for 15 minutes. 

**9.** **Dilute Klenow Fragment 5-fold** in water and combine pre-nicked template reaction with polymerase mix. <br/> _Remaining components can be assembled on ice as master mix._ 

  | Component | [Stock] | Quantity | 
  | ---------: | :---------: |:---------- |  
  | pre-nicked template || **20**  µL |   
  | RNase-free water|| **15.5**  µL |
  | NEB Buffer 3.1 | 10X | **2**  µL |
  | dNTP mix | 1 mM each | **10**  µL |
  | DTT | 100 mM | **1**  µL |
  | T4 Gene 32 Protein | 10 mg/ml | **0.5**  µL |
  | Klenow Fragment | **1 U/µL** | **1**  µL |
  | **Total** || **50** µL |
  <br/>

**10.** Incubate reactions at 35 °C and remove 15 uL at varying time points. <br/> A good starting point is 30 min, 1 hour, and 2 hours.

**11.** At each time point, inactivate enzymes at 80 °C for 20 minutes. <br/> Move inactivated time points to 4 °C until ready to clean up all samples.

<br/><br/><br/><br/><br/><br/><br/><br/>

### SPRI bead cleanup and Tape (~40 minutes)

**12.** Dilute reaction products to 30 µL and clean up with 1.8X SPRI beads and 3 75 % ethanol washes. <br/> Elute products in 16 µL of water.

**13.** Use a spec to measure concentrations and analyze products on an HS D1000 Tape.

### qPCR follow-up

**14.** Make 1:1000 dilutions of each sample and measure increase in desired products by qPCR. <br/> Choose the time point where signal plateaus.
