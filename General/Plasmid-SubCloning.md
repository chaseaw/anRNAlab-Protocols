Double Restriction Enzyme Plasmid Sub-Cloning
================================================================================
This is a general protocol for how to digest an existing plasmid, and re-ligate with 
an insert. Check out the Lab Benchling for the Plasmid Database (https://benchling.com/bowbritt/f_/8mJrYOJH-plasmid-database/) 
and pTETRIS Expression vectors (https://benchling.com/cweidmann/f_/7cICZyyi-ptetris-expression-vectors/) for possible backbones.


Useful symbols: µ°

Materials
--------------------------------------------------------------------------------
  * Q5 PCR Materials  
    ◦ Q5 2X Buffer   
    ◦ Forwards + Reverse Primers with Restriction Enzyme Sites  
    ◦ Input DNA or cDNA
  * Restriction Enzymes
  * rCutSmartBuffer
  * PCR Clean-Up Kit (NEB Monarch https://www.neb.com/en-us/products/t1030-monarch-pcr-dna-cleanup-kit-5-ug?srsltid=AfmBOoosHMyYJYZayyvPRfYxAON-PB7djlwKAoBYeznQUNVmWk2iVVRW) OR SPRI Beads
  * Gel Purification Kit (NEB Monarch https://www.neb.com/en-us/products/t1120-monarch-spin-dna-gel-extraction-kit)
  *  

Equipment Required
--------------------------------------------------------------------------------
  * Thermocycler
  * Microcentrifuge


<br/><br/><br/><br/><br/><br/><br/>


___
Protocol:
--------------------------------------------------------------------------------
**Digesting Insert (~1.5 hrs)** 

**1.** Prepare a 25 uL Q5 PCR reaction to append the restriction enzyme (RE) sites to the ends of your DNA of interest, and run for 25-30 cycles.

 **2.** Use the PCR Clean-up kit or SPRI beads (adjust ratio based on product size) to clean-up the resulting product

 **3.** Validate the expected product was produced by speccing, and running a TAPE

 **4.** Set up a restriction enzyme digest for the insert. Be sure to know your insert length.
| Component | Concentration | Quantity | 
  | ---------: | ---------: | :---------- |
  | DNA | 250-500 ng (depends on insert size)  | **X**  µL | 
  | NEB rCutSmart Buffer | 10X | 5  µL |
  | Restriction Enzyme (s) |Usually, 20 U/uL| **Y**  µL |
  | Nuclease Free Water || Up to 25  µL |
  || **Total** | 25 µL |
 
 *The DNA input does not necessarily have to be ~500 ng; could be scaled up or down*
 *Y: see your RE information about how many units are necessary to digest your insert. In general, NEB recommends 5–10 units of enzyme per µg DNA, and 10–20 units for genomic DNA in a 1 hour digest. 1 µL is a good starting point. Plasmid inserts are usually significantly shorter than a plasmid or genomic DNA, and therefore usually less RE is necessary.*

 **5.** Run the RE digest at 37°C for an hour (Check to see if your RE has different conditions), and heat inactivaate as necessary.

 **6.** Clean up the insert with PCR Clean-Up or SPRI beads. Validate concentration with a spec.


 **Digesting and Purifying Plasmid Backbone (~2.5hrs)**

**1.** Set up a restriction enzyme (RE) digest of the plasmid backbone. If you need a large amount of backbone for multiple ligation reactions, set up multiple digestions. Since multiple REs will be used, it is STRONGLY encouraged to have single RE control samples, to ensure the REs are functional. Be sure to know the length of your plasmid.
| Component | Concentration | Quantity | 
  | ---------: | ---------: | :---------- |
  | DNA | 1 µg  | **X**  µL | 
  | NEB rCutSmart Buffer | 10X | 1  µL |
  | Restriction Enzyme (s) |Usually, 20 U/uL| **Y**  µL |
  | Nuclease Free Water || Up to 10  µL |
  || **Total** | 10 µL |
  
*The DNA input does not necessarily have to be ~500 ng; could be scaled up or down*
 *Y: see your RE information about how many units are necessary to digest your insert. In general, NEB recommends 5–10 units of enzyme per µg DNA, and 10–20 units for genomic DNA in a 1 hour digest. 1 µL is a good starting point.*

 **2.** Run the RE digest at 37°C for an hour (Check to see if your RE has different conditions). Heat inactive *only* if the only item you need is the plasmid backbone.

 **3.** While this is running, pour a 1% agarose gel with the smallest combs (12 wells) for downstream gel purification of the backbones.

If the plasmid does not have an insert you also plan to isolate and religate, you must do a dephosphorylation of the 5′ ends of the plasmid (CIP), to ensure it does not reseal without accepting the insert.  Remeber, if both the insert and the backbone at dephosphorylated, the plasmid will not re-ligate!

 **4.** Add 1 µL of Quick CIP to the RE reaction, and incubate for another 10 min at 37°C. 

 **5.** Heat inactivate *both* the CIP at 80°C for 2 minutes, and the RE enzymes?

 If the insert is being isolated for ligation later, do not CIP the digestion reaction

 **6.** Run your multi- and single digested plasmid, along with an undigested control on the gel. 90V for an hour should be sufficient.

 **7.** Cut out the plasmid backbone (and insert, if applicable), then gel purify the slices via Monarch NEB Gel Purification Spin Kit. If you have multiple reactions to increase yield, pool all the samples into one column (up to 5 µg), and elute into 20 µl Validate concentration via spec.

**Optional CIP Reaction (~1.5hrs)**

If you are also attempting to isolate the plasmid insert for downstream uses in plasmid cloning, you must do a dephosphorylation reaction after the backbone has been isolated. 

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
  <!-- : in the pipes specify justification -->
  <!-- **X** bolds the inside -->
<!-- The text below creates dropdown lists for links to next steps or hyperlinks -->

<details>
  <summary>Next Steps</summary>
  
</p> <a href="./path-to-file/file1.ext">
LINK1 NAME</a>

</p> <a href="./path-to-other-file/file2.ext">
LINK2 NAME</a>

</details>

<details>
  <summary>More Info</summary>
  
  <a href="https://www.website.com/just-copy-paste-your-target-website-here.html">
WEBSITE LINK NAME</a>  

</details>
