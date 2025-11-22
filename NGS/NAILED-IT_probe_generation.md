Probe generation for NAILED-IT
================================================================================
Description: Find optimal time conditions for new NAILED-IT probesets  
(Nickase-Activated Iterative Linear Extension of DNA for Isolating Targets)

Materials:
--------------------------------------------------------------------------------
  * 10 ng/µl (240 nM) of TS probe template pool <br/> _Templates should end in sequence complementary to RC and not include Nt.BspQI sites._
  * 200 nM TEQUILA-SEQ universal reverse complement oligo([ARL1050](../ARL-primers.csv))
  * 1 mM dNTP mix (each nucleotide at 1 mM, with 2:1 dTTP:Bio-16-dUTP for final reactions)
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

**1.** Combine the following components on ice in the indicated order (add buffer last).<br/>
_Note: After finding optimal timing, final probe generation can be done at 4X volumes._<br/>

  | Component | [Stock] | Optimizing | For final |
  | ---------: | :---------: | :---------- | :---------- |
  | template pool | 10 ng/µl | **1**  µL |  **4**  µL |
  | RC oligo | 200 nM | **1**  µL | **4**  µL |
  | dNTP mix | 1 mM each | **12.5**  µL | **50**  µL |
  | RNase-free water || **25**  µL | **100**  µL |
  | SDA Buffer | 10X | **5**  µL | **20**  µL |
  | **Total** || **44.5** µL | **178**  µL |
  <br/>
  
**2.** Anneal RC oligo to template pool in a thermocycler with the following program:  

  | Temp | Time | Step |
  | :--------: | :---------: |:---------: |
  | **95 °C** | **2:00** | **inital denaturation** |
  | **down to 4 °C** | **0.1 °C/sec** | **gradual ramp down** |
  | **4 °C** || **hold until next step** |
  
  _Note: Should take 15 minutes to ramp down from 95 to 4,_ <br/> _set Proflex ramp rate to 0.3 °C/sec to achieve this._

<br/><br/><br/><br/><br/><br/>

### Intial extension (~15 minutes)

**3.** To each sample, add the following components: <br/> _Tip: can spot 1 µL at tube tops and spin down to mix_

  | Component | [Stock] | Optimizing | For final |
  | ---------: | :---------: | :---------- | :---------- |
  | annealed mix || **44.5**  µL |  **178**  µL |
  | DTT | 100 mM | **1**  µL | **4**  µL |
  | T4 Gene 32 Protein | 10 mg/ml | **1**  µL | **4**  µL |
  | Klenow Fragment| 5 U/µL | **2.5**  µL | **10**  µL |
  | **Total** || **49** µL | **196**  µL |
  <br/>

**4.** Incubate extension in a thermocycler for 10 minutes at 37 °C (set lid to 55 °C)

### Isothermal strand displacement amplification (6 hours to O/N)

### If optimizing timing:

**5a.** Remove 7.8 µL of the mixture and incubate separately at 37 °C. <br/>

**6a.** To remaining reaction, add 0.84 µL of Nt.BspQI nickase diluted 5-fold (to 2U/µL).<br/>

**7a.** Immediately remove 8 µL and add to 16 µL of 2X RNA loading dye. <br/> This is time zero.

**8a.** Incubate remaining reaction at 37 °C, removing 8 µL aliquots at varying time points. <br/> A good starting point is 1, 2, 4, and 6 hours.

**9a.** At each time point, inactivate 8 µL aliquots with 16 µL of 2X RNA loading dye. <br/> Move inactivated time points to 4 °C until ready to run all samples. <br/>
_Note: the no nickase control should incubate as long as the longest time point._

<br/><br/><br/>

### If performing final amplifications:

**5b.** To remaining reaction, add 4 µL of Nt.BspQI nickase diluted 5-fold (to 2U/µL).<br/>

**6b.** Incubate reaction at 37 °C for optimized time.

**7b.** Inactivate enzymes at 80 °C for 20 minutes.

**8b.** Clean and concentrate sample to 30 µL with a Zymo kit.

**9b.** Purify away unwanted byproducts using a 2-step SPRI strategy. <br/>
Use 1.5X beads, take S/N and increase to 3X beads + 1.8X isopropanol. <br/>
Elute in 17 µL and prepare 1 µL for gel verification (+ 7µL water, + 16µL 2X dye).

### Denaturing PAGE analysis

**10.** Denature samples at 70 °C for 5 minutes then rapidly cool to 4 °C. <br/> _Great time to set up urea gel, flush wells, and pre-run_

**11.** Load samples onto TBE-urea gel and run ~180 V for 45 minutes in 1X TBE.

**12.** post-stain gel in 1X SYBR Gold in TBE for 15 minutes and image.
