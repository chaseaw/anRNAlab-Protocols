Optimization of probe generation for TEQUILA-SEQ
================================================================================
Description: Find optimal time conditions for new TS probesets

Materials:
--------------------------------------------------------------------------------
  * 10 ng/µl of TS probe template pool <br/> _Templates should end in sequence complementary to RC and not include Nt.BspQI sites._
  * 2 µM TEQUILA-SEQ universal reverse complement oligo([ARL1050](../ARL-primers.csv))
  * 1 mM dNTP mix (each nucleotide at 10 mM)
  * **10X NEBuffer 3.1 (~pH 7.9 at RT, included with nickase enzyme)**
    * 500 mM Tris-HCl
    * 1 M NaCl
    * 100 mM MgCl<sub/>2<sub>
    * 100 µg/ml BSA
  * 100 mM DTT
  * 10 mg/ml (~298 µM) [T4 Gene 32 Protein](https://www.neb.com/en-us/products/m0300-t4-gene-32-protein) (single standed DNA binding protein)
  * 5 units/µl (~14.7 µM) [Klenow Fragment (3´→5´ exo-)](https://www.neb.com/en-us/products/m0212-klenow-fragment-3-5-exo)
  * 10 units/µl [Nt.BspQI nickase](https://www.neb.com/en-us/products/r0644-ntbspqi) 
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

**1.** Combine the following components on ice in the indicated order (add buffer last). <br/> Assemble enough for 5 reactions (4 time points + 1 no nickase control)

  | Component | [Stock] | Quantity | 
  | ---------: | :---------: |:---------- |
  | template pool | 10 ng/µl | **1**  µL | 
  | RC oligo | 2 µM | **5**  µL |
  | dNTP mix | 1 mM each | **10**  µL |
  | RNase-free water|| **25.5**  µL |
  | NEB Buffer 3.1| 10X | **5**  µL |
  | **Total** || **46.5** µL |
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

### Intial extension (~15 minutes)

**3.** To each sample, add the following components: <br/> _Tip: can spot 1 µL at tube tops and spin down to mix_

  | Component | [Stock] | Quantity | 
  | ---------: | :---------: |:---------- |
  | annealed mix || **46.5**  µL | 
  | DTT | 100 mM | **1**  µL |
  | T4 Gene 32 Protein | 10 mg/ml | **1**  µL |
  | Klenow Fragment| 5 U/µL | **0.5**  µL |
  | **Total** || **49** µL |
  <br/>

**4.** Incubate extension in a thermocycler for 10 minutes at 37 °C (set lid to 55 °C)

### Isothermal strand displacement amplification (up to 16 hours)

**5.** For each time point sample, add 1 µL of Nt.BspQI nickase diluted 5-fold (to 2U/µL). <br/> For the no nickase control, add 1 µL of water.

**6.** Incubate reactions at 40 °C for varying time points. <br/> A good starting point is 2, 4, 6, and 8 hours.

**7.** At the end of each time point, inactivate enzyme at 80 °C for 20 minutes. <br/> Move inactivated time points to 4 °C until ready to clean up all samples. <br/> _Note: the no nickase control should incubate as long as the longest time point._

<br/><br/><br/><br/><br/><br/><br/><br/>

### Day 2: Purification and analysis

### SPRI bead cleanup and Tape (~40 minutes)

**8.** Clean up reaction products with 1.8X SPRI beads and 2 75 % ethanol washes. <br/> Elute products in 30 µL of water.

**9.** Use a spec to measure concentrations and analyze products on an HS D1000 Tape. <br/> The no nickase control should only show initial extension products at correct size, <br/> longer time points should have more products (smears).

### qPCR follow-up

**10.** Make 1:1000 dilutions of each sample and measure increase in desired products by qPCR. <br/> Choose the time point where signal plateaus.
