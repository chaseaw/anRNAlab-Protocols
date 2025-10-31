Double Restriction Enzyme Plasmid Sub-Cloning
================================================================================
This is a general protocol for how to digest an existing plasmid, and re-ligate with 
an insert. Check out the Lab Benchling for the Plasmid Database (https://benchling.com/bowbritt/f_/8mJrYOJH-plasmid-database/) 
and pTETRIS Expression vectors (https://benchling.com/cweidmann/f_/7cICZyyi-ptetris-expression-vectors/) for possible backbones.

Materials
--------------------------------------------------------------------------------
  * [Q5 PCR Materials](https://www.neb.com/en-us/products/m0492-q5-high-fidelity-2x-master-mix) or equivalent PCR reagents  
    ◦ Q5 2X Master Mix Buffer   
    ◦ 10 µM each Forward + Reverse Primers with Restriction Enzyme Sites  
    ◦ Template DNA or cDNA
  * NEB Restriction Enzymes
  * rCutSmartBuffer
  * PCR Clean-Up Kit ([NEB Monarch](https://www.neb.com/en-us/products/t1030-monarch-pcr-dna-cleanup-kit-5-ug)) OR SPRI Beads
  * Gel Purification Kit ([NEB Monarch](https://www.neb.com/en-us/products/t1120-monarch-spin-dna-gel-extraction-kit))
  * **10X T4 DNA Ligation Buffer** (pH 7.5 @ 25°C)  
    ◦ 500 mM Tris-HCl  
    ◦ 100 mM MgCl2  
    ◦ 10 mM ATP  
    ◦ 100 mM DTT   
  * [T4 DNA Ligase (2000 U/µL)](https://www.neb.com/en-us/products/m0202-t4-dna-ligase)

Equipment Required
--------------------------------------------------------------------------------
  * Thermocycler
  * Microcentrifuge

___
Protocol:
--------------------------------------------------------------------------------
**Amplification and Digestion of Insert (~1.5 hrs)** 

**1.** Prepare a 25 uL Q5 PCR reaction to append the restriction enzyme (RE) sites to the ends of your DNA of interest, and run for 25-30 cycles.

 **2.** Use the PCR Clean-up kit or SPRI beads (adjust ratio based on product size) to purify the resulting product.

 **3.** Validate the expected product size by gel or TapeStation.

 **4.** Set up a restriction enzyme digest for the insert. Be sure to know your insert length. <br/> 
 _Note: a Unit is defined as enzyme required to cut 1 µg single site plasmid (~3kb) in 1 hour._ <br/>
 _You will want 3000/insert length*5 units to ensure complete digestion per µg insert in 1 hour._
| Component | Concentration | Quantity | 
  | ---------: | ---------: | :---------- |
  | DNA | 250-500 ng | **X**  µL | 
  | NEB rCutSmart Buffer | 10X | 2.5  µL |
  | Restriction Enzyme (s) |Usually 20 U/uL| **Y**  µL |
  | Nuclease Free Water || Up to 25  µL |
  || **Total** | 25 µL |
 
 *The DNA input does not necessarily have to be ~500 ng; could be scaled up or down*
 
 *Y: Total restriction enzyme added should not exceed 10 % of the total volume.*

 **5.** Run the RE digest at 37°C for an hour (Check to see if your RE has different conditions), and heat inactivate as necessary.

 **6.** Clean up the insert with PCR Clean-Up or SPRI beads. Measure concentration with a spectrophotometer.


 **Digesting and Purifying Plasmid Backbone (~2.5hrs)**

**1.** Set up a restriction enzyme (RE) digest of the plasmid backbone. If you need a large amount of backbone for multiple ligation reactions, set up multiple digestions. Since multiple REs will be used, it is STRONGLY encouraged to have single and no RE control samples, to ensure the REs are functional. Be sure to know the length of your plasmid.
| Component | Concentration | Quantity | 
  | ---------: | ---------: | :---------- |
  | DNA | 1 µg  | **X**  µL | 
  | NEB rCutSmart Buffer | 10X | 1  µL |
  | Restriction Enzyme (s) |Usually, 20 U/uL| **Y**  µL |
  | Nuclease Free Water || Up to 10  µL |
  || **Total** | 10 µL |
  
*The DNA input does not necessarily have to be ~500 ng; could be scaled up or down*

 **2.** Run the RE digest at 37°C for an hour (Check to see if your RE has different conditions). Heat inactivate *only* if the only item you need is the plasmid backbone.

 **3.** While this is running, pour a 1% agarose gel with the smallest combs (12 wells) for downstream gel purification of the backbones.

 _It helps to dephosphorylate the 5′ ends of the plasmid (CIP) to prevent sealing without an insert during ligation._ <br/> _Unless you plan on using a cut out insert to subclone, you can add CIP directly after digestion._

 **4.** Add 1 µL of Quick CIP to the RE reaction, and incubate for another 10 min at 37°C. 

 **5.** Heat inactivate 80°C for 2 minutes. This should inactivate the CIP and the REs.

 _If the insert is being isolated for ligation later, do not CIP the digestion reaction!_

 **6.** Run your multi-, single, and undigested digested plasmid on the gel. 90V for an hour should be sufficient.

 **7.** Cut out the plasmid backbone (and insert, if applicable), taking care to minimize exposure to the light. <br/>
 Gel purify the slices via Monarch NEB Gel Purification Spin Kit. <br/>
 If you have multiple reactions: to increase yield, pool all the samples into one column (up to 5 µg) and elute into 20 µl. Measure concentration.

**Optional CIP Reaction (~0.5hrs)**

_If you are also attempting to isolate the plasmid insert for downstream uses in plasmid cloning, you must dephosphorylate the backbone separately._ 

**1.** Setup the following reaction with the *digested plasmid backbone*.
| Component | Concentration | Quantity | 
  | ---------: | ---------: | :---------- |
  | Plasmid Backbone | variable  | 17  µL | 
  | NEB rCutSmart Buffer | 10X | 2  µL |
  | Quick CIP || 1  µL |
  | Nuclease Free Water || Up to 20  µL |
  || **Total** | 20 µL |

*Technically, CIP acts on 1 pmol of DNA ends, but 1 µL is usually enough; adjust if concentration is particularly high*

**2.** Heat for 10 min at 37°C, then heat inactivate for 2 minutes at 80°C

**3.** PCR Clean-Up the backbone

**Ligation Reaction (30 min + overnight)**
  
  **1.** Thaw the T4 Ligase + ATP Buffer at room temperature, frequently pipetting up and down to ensure full resuspension.

  **2.** Prepare the following ligation reaction. *Using a water/buffer master mix is highly encouraged*

https://nebiocalculator.neb.com/#!/ligation
  
| Component | Concentration | Quantity | 
  | ---------: | ---------: | :---------- |
  | Plasmid Backbone | variable  | ~50-100 ng |
  | Insert | variable  | 3 molar equivalents of backbone | 
  | T4 Ligase Buffer | 10X | 2  µL |
  | Ligase || 1  µL |
  | Nuclease Free Water || Up to 20  µL |
  || **Total** | 20 µL |

  *Formally, it should be 0.02pmol of backbone to 0.06 pmol of insert, but the ratio is more important. Use the NEB Ligation calculator to calculate molar equivelnt*

  **3.** Incubate overnight at 16°C, then heat inactivate the next day for 20 minutes at 65°C.

  

<details>
  <summary>Next Steps</summary>
  
</p> <a href="./Transforming-Compotent-Cells.md">
Transforming Compotent Cells</a>

</details>

<details>
  <summary>More Info</summary>
  
  <a href="https://www.website.com/just-copy-paste-your-target-website-here.html](https://www.neb.com/en-us/tools-and-resources/usage-guidelines/cloning-guide?srsltid=AfmBOoocwspyvZkT2YmG7L6xBMkEeglV3-dzmP6ptGuqFeQIJb9pek5m">
NEB Cloning Info</a>  

</details>
