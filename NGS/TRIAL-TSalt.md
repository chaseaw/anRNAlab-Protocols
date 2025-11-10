Optimization of probe generation for TEQUILA-SEQ
================================================================================
Description: Find optimal time conditions for new TS probesets

Materials:
--------------------------------------------------------------------------------
  * 10 ng/µl (240 nM) of TS probe template pool <br/> _Templates should end in sequence complementary to RC and not include Nt.BspQI sites._
  * 200 nM TEQUILA-SEQ universal reverse complement oligo([ARL1050](../ARL-primers.csv))
  * 1 mM dNTP mix (each nucleotide at 1 mM)
  * **10X SDA Buffer (~pH 8.0 at RT)**
    * 400 mM Tris-HCl pH 8
    * 500 mM NaCl
    * 100 mM MgCl<sub/>2<sub>
    * 1 mg/ml BSA
  * 100 mM DTT
  * 10 mg/ml (~298 µM) [T4 Gene 32 Protein](https://www.neb.com/en-us/products/m0300-t4-gene-32-protein) (single standed DNA binding protein)
  * 5 units/µl (~14.7 µM) [Klenow Fragment (3´→5´ exo-)](https://www.neb.com/en-us/products/m0212-klenow-fragment-3-5-exo)
  * 10 units/µl [Nt.BspQI nickase](https://www.neb.com/en-us/products/r0644-ntbspqi) 
  * [RNA Loading Dye (2X)](https://www.neb.com/en-us/products/b0363-rna-loading-dye-2x) 
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

### Template-RC annealing (~30 minutes)

**1.** Combine the following components on ice in the indicated order (add buffer last).

  | Component | [Stock] | Quantity | 
  | ---------: | :---------: |:---------- |
  | template pool | 10 ng/µl | **1**  µL | 
  | RC oligo | 200 nM | **1**  µL |
  | dNTP mix | 1 mM each | **12.5**  µL |
  | RNase-free water || **25**  µL |
  | SDA Buffer | 10X | **5**  µL |
  | **Total** || **44.5** µL |
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
  | annealed mix || **44.5**  µL | 
  | DTT | 100 mM | **1**  µL |
  | T4 Gene 32 Protein | 10 mg/ml | **1**  µL |
  | Klenow Fragment| 5 U/µL | **2.5**  µL |
  | **Total** || **49** µL |
  <br/>

**4.** Incubate extension in a thermocycler for 10 minutes at 37 °C (set lid to 55 °C)

### Isothermal strand displacement amplification

**5.** Remove 7.8 µL of the mixture and incubate separately at 37 °C. <br/> This is the no nickase control.

**6.** To remaining reaction, add 0.84 µL of Nt.BspQI nickase diluted 5-fold (to 2U/µL).

**7.** Immediately remove 8 µL and add to 16 µL of 2X RNA loading dye. <br/> This is time zero.

**8.** Incubate remaining reaction at 37 °C, removing 8 µL aliquots at varying time points. <br/> A good starting point is 10, 20, 40, and 80 minutes.

**9.** At each time point, inactivate 8 µL aliquots with 16 µL of 2X RNA loading dye. <br/> Move inactivated time points to 4 °C until ready to clean up all samples. <br/> _Note: the no nickase control should incubate as long as the longest time point._

<br/><br/><br/><br/><br/><br/><br/><br/>

### Denaturing PAGE analysis

**10.** Denature samples at 70 °C for 5 minutes then rapidly cool to 4 °C. <br/> _Great time to set up urea gel, flush wells, and pre-run_

**11.**  Load samples onto TBE-urea gel and run ~180 V in 1X TBE.

**12.** post-stain gel in 1X SYBR Gold in TBE for 20 minutes and image.
