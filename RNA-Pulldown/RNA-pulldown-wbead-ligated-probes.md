RNA pulldown with bead-ligated DNA oligo probes
================================================================================
Description: Capture target RNAs from total using bead-ligated DNA oligos

[Go To Protocol](#protocol)

Materials:
--------------------------------------------------------------------------------
  ◦ 10 µg Input RNA  
  ◦ 100 µM splint-complementary probe mixes _(AS to target and control (U1) probes)_  
  ◦ 1 mM polyA splint DNA [ARL1158](../ARL-primers.csv)  
  ◦ 10 units/µl [T4 Polynucleotide Kinase](https://www.neb.com/en-us/products/m0201-t4-polynucleotide-kinase)  
  ◦ [Oligo d(T)<sub>25</sub> Magnetic Beads](https://www.neb.com/en-us/products/s1419-oligo-dt25-magnetic-beads)  

  * **[T4 DNA Ligase Reaction Buffer (10X)](https://www.neb.com/en-us/products/b0202-t4-dna-ligase-reaction-buffer)**   
    ◦ 500 mM Tris pH 7.5  
    ◦ 100 mM MgCl<sub>2</sub>  
    ◦ 10 mM rATP 
    ◦ 100 mM DTT 

  * **HEPES Buffer Base (10X)** _(can be stored long term)_   
    ◦ 500 mM HEPES pH 7.5  
    ◦ 25 mM EDTA 

  * **Tris Buffer Base (10X)** _(can be stored long term)_   
    ◦ 100 mM Tris pH 7.5  
    ◦ 25 mM EDTA 

Equipment Required:
-------------------------------------------------------------------------------- 
◦ Magnetic rack  
◦ Heat block with shaking  
◦ Thermocycler  

<br/><br/> 

Day of Buffer Preparation:
-------------------------------------------------------------------------------- 
  * **oligo dT Wash Buffer**  
    ◦ 1X HEPES Buffer Base  
    ◦ 300 mM NaCl 
    ◦ 0.1 % Triton X-100 

  * **oligo dT Binding Buffer** 
    ◦ 1X HEPES Buffer Base  
    ◦ 500 mM LiCl 
    ◦ 0.1 % Triton X-100 

  * **Quick Ligation Mix (2X)**  
    ◦ 2.5X NEBNext® Quick Ligation Reaction Buffer [(from 5X)](https://www.neb.com/en-us/products/b6058-nebnext-quick-ligation-reaction-buffer)  
    ◦ 0.625X Instant Sticky-end Ligase Master Mix [(from 2X)](https://www.neb.com/en-us/products/m0370-instant-sticky-end-ligase-master-mix)  
    ◦ 18.75 % 1,2 propanediol _(CAS#57-55-6)_  

  * **TE elution Buffer**  
    ◦ 1X Tris Buffer Base  
    ◦ 10 mM **additional** Tris pH 7.5  
    ◦ 0.1 % SDS  

  * **4M Urea Hybridization Buffer**  
    ◦ 1X Tris Buffer Base  
    ◦ 4M Urea 
    ◦ 2.5 mM **additional** EDTA  
    ◦ 500 mM LiCl  
    ◦ 0.5 % Triton X-100  
    ◦ 0.2 % SDS  
    ◦ 0.1 % Sodium Deoxycholate  

  * **SDS Wash Buffer**  
    ◦ 1X HEPES Buffer Base  
    ◦ 7.5 mM **additional** EDTA  
    ◦ 10 % SDS  

<br/>



Protocol:
--------------------------------------------------------------------------------
**Part 1: Kinase probes and prepare beads (1.5 hours)**

**1.** Assemble a kinase reaction for each capture sample.<br/>
_Note: Be sure to include samples for capture with U1 control probes._

  | Component | Concentration | Quantity | 
  | ---------: | ---------: | :---------- |
  | probes | 100 µM | **10**  µL | 
  | RNase-free water | | **5.5**  µL |
  | T4 Ligase Buffer | 10X | **2**  µL |
  | T4 PNK  | 10 U/µl | **2**  µL |  
  || **Total** | **20** µL |
  
**2.** Incubate the reaction for 1 hour at 37 °C.<br/>
While samples are kinased, prepare buffers for bead equilibration:<br/>
Per capture: 600 µl of dT Wash Buffer, 100 µl of dT Binding Buffer

**3.** During kinase incubation, prepare Oligo d(T)<sub>25</sub> magnetic beads:<br/>
Aliquot 50 µl bead slurry per capture. Capture beads and remove liquid.

**4.** Wash beads twice (suspending beads each time) in 50 µl dT Wash Buffer.

**5.** Resuspend beads in 25 µl of dT Binding Buffer. Add 1 µl of 1 mM polyA splint.

**6.** Incubate at 25 °C with 1000 rpm shaking for 30 minutes.

**7.** Wash beads three times with 50 µl dT Wash Buffer.<br/>
_Don't remove the last wash until the PNK reaction is finished._

<br/>
**Part 2: Splinted ligation of probes to beads (1 hour)**

**8.** Prepare 25 µl of 2X Quick Ligation Mix per capture.

**9.** Resuspend beads in 20 µl of PNK reaction and 20 µl of 2X Quick Ligation Mix.

**10.** Incubate at 25 °C with 1250 rpm shaking for 30 minutes.<br/>
While beads are ligated, prepare buffers for bead equilibration:<br/>
Per capture: 400 µl of TE Elution, 600 µl of 4M Urea Hyb, 200 µl SDS Wash

**11.** Wash beads three times with 50 µl dT Wash Buffer:<br/>
each wash should be 2 min at 95 °C with 1250 rpm shaking.

**12.** Wash beads three times (quick at RT) with 50 µl 4M Urea Hyb.

**13.** Resuspend beads in 25 µl of 4M Urea Hyb Buffer.

<br/>
**Part 3: RNA Capture (1.5 hours for single capture/3 hours for double capture)**

**14.** Mix 10 µg of RNA into 200 µl of 4M Urea Hyb Buffer and pre-warm to 42 °C.

**15.** Add RNA mix to 25 µl of ligated beads.<br/>
_Note: If performing a double capture, use 12.5 µl beads for each sequential capture._

**16.** Hybridize to beads at 42 °C for 30 minutes with 1000 rpm shaking.<br/>
_In theory, flowthrough could be added to other probe-beads to capture other targets._

**17.** Perform the following washes to bound beads:<br/>
2X 50 µl washes with **4M Urea Hyb**, 2 minutes at 37 °C with 1100 rpm shaking  
2X 50 µl washes with **SDS Wash**, 2 minutes at 37 °C with 1100 rpm shaking  
2X 50 µl washes with **dT Wash**, 2 minutes at 37 °C with 1100 rpm shaking  
2X 50 µl washes with **TE Elution**, quick washes at RT

**18.** Resuspend beads in 15 µl TE Elution,<br/>
Heat 3 minutes at 95 °C with 1350 rpm shaking.<br/>
Retain first elution, repeat 15 µl elution with beads,<br/>
combine first and second elution for a total of 30 µl.<br/>
_Note: If performing double capture, take elution to step 14 and repeat._

<br/>
**Part 4: qPCR validation (2.5 hours)**

**19.** Perform qPCR of target on Input RNA and elution to confirm enrichment.

<details>
  <summary>Next Steps</summary>
  
</p> <a href="../Mutational-Profiling/MaP-RT-SSII.md">
MaP with SuperScript II RT</a>

</p> <a href="../NGS/Second-Strand-Synthesis.md">
Second-Strand Synthesis</a>

</p> <a href="../NGS/Basic-Nextera-XT.md">
Nextera XT library prep</a>

</details>

<details>
  <summary>Cited Protocols</summary>
  
  <a href="https://doi.org/10.1101/2025.11.23.690051">
RAPMS 2.0 Improves Specificity and Throughput for Proteomic Identification of</a> <br/>RNA Binding ProteinsToehold techology, wash buffers, capture oligos. 
<br/>

</details>
