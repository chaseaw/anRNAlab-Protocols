Nextera library preparation for whole-plasmid sequencing
================================================================================
Description: Using "tagmentation" workflow to fragment and index plasmids for next-gen sequencing.

Reagent volumes have been dramatically reduced from manufacturer's guidelines for cost-savings.

Materials:
--------------------------------------------------------------------------------
  * Diluted plasmid (0.1 ng/µL)
  * Illumina Nextera XT reagents
    * Tagment DNA Buffer
    * Amplicon tagment mix
    * Neutralization Buffer
    * Nextera PCR Master Mix
  * [In-house index primers](../CWML-primers.csv)
    * In-house index primer F (i7, 5 µM)
    * In-house index primer R (i5, 5 µM)
  * Magnetic SPRI beads [(Omega BioTek)](https://www.omegabiotek.com/product/mag-bind-totalpure-ngs/?gclid=CjwKCAiA1eKBBhBZEiwAX3gqlw2-fi_geWTPQcJVkZdR--dL3zrHwdkoLxc-VhABYCzBcpVGy-4v7BoCtjgQAvD_BwE&cn-reloaded=1)

Equipment Required:
--------------------------------------------------------------------------------
  * Thermocycler
  * Magnetic Stand
  
___
Protocol:
--------------------------------------------------------------------------------

**1.** Set up tagmentation reactions for each plasmid:

  | Component | Concentration | Quantity | 
  | ---------: | ---------: | :---------- |
  | Tagment DNA Buffer | 2X | **2.5**  µL | 
  | plasmid DNA | 0.1 ng/µL | **1.25**  µL |
  | Amplicon Tagment Mix || **1.25**  µL |
  || **Total** | **5** µL |
  
  <!-- : in the pipes specify justification -->
  <!-- **X** bolds the inside -->
  
 **2.** In a thermocycler, incubate reactions at 55 °C for 11 minutes, then cool to 10 °C.
   * *Note: Normal reaction time is 5 minutes, but plasmids are much longer than typical template* 

**3.** As soon as reactions reach 10 °C, add 1.25 µL Neutralization Buffer (NT) and incubate 5 min at RT.
  * *Neutralization buffer stops the reaction, so timing is important*
  
**4.** Assemble Nextera PCR reactions:

  | Component | Concentration | Quantity | 
  | ---------: | ---------: | :---------- |
  | Tagmented DNA | | **6.25**  µL | 
  | i7 index primer | 5µM | **1.25**  µL |
  | i5 index primer | 5µM | **1.25**  µL |
  | Nextera PCR Master Mix |3.33X| **3.75**  µL |
  || **Total** | **12.5** µL |
  
**5.** Run Nextera PCR:

  | Cycles | Temp | Time | Step |
  | ---------: | :--------: | :---------: |:---------: |
  | **1** | **72 °C** | **3:00** | **overhang repair** |
  | **1** | **95 °C** | **0:30** | **inital denaturation** |
  
  || 95 °C | 0:10 | denaturation |
  | ---------: | :--------: | :---------: |:---------: |
  | **-14X-** | **55 °C*** | **0:30** | **annealing** |
  || **72 °C** | **0:30** | **extension** |
 
  | 1 | 72 °C | 5:00 | final extension |
  | ---------: | :--------: | :---------: |:---------: |

*Note: Cycle number has been increased by 2 to offset the use of less reagent*

**6.** Clean up PCRs with columns or SPRI beads. Elute libraries in 15 µL of water.
  * Dilute with 17.5 µL of water and use [SPRI beads](./SPRI-beads.md) to purify (0.65X ratio and 2X washes with 80% ethanol).
  * Alternatively, add 17.5 µL of TE buffer to PCR products and purify with [column-based kit](https://www.neb.com/-/media/nebus/files/protocols/t1030_quick_protocol_card_monarch_pcrdna_cleanup.pdf?rev=df342b32fb1144af88257b50773a0c7a&hash=662C2FB4EA8277B53B4FE89E3D5887A8)
  
**7.** Check samples on a Bioanalyzer/TapeStation and assess length distributions before sequencing.

  
<!-- The text below creates dropdown lists for links to next steps or hyperlinks -->

<details>
  <summary>More Info</summary>
  
  <a href="https://support.illumina.com/content/dam/illumina-support/documents/documentation/chemistry_documentation/samplepreps_nextera/nextera-xt/nextera-xt-library-prep-reference-guide-15031942-05.pdf">
Detailed Nextera Information</a>

<br/>

  <a href="https://www.neb.com/-/media/nebus/files/protocols/t1030_quick_protocol_card_monarch_pcrdna_cleanup.pdf?rev=df342b32fb1144af88257b50773a0c7a&hash=662C2FB4EA8277B53B4FE89E3D5887A8">
Monarch DNA Cleanup (NEB)</a> 

</details>
