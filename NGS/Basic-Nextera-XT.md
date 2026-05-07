Nextera XT library preparation for sequencing
================================================================================
Description: Using "tagmentation" workflow to fragment and index DNA libraries for next-gen sequencing.

Materials:
--------------------------------------------------------------------------------
  * Diluted dsDNA (0.2 ng/µL)
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

<br/><br/><br/><br/><br/><br/><br/><br/>
___
Protocol:
--------------------------------------------------------------------------------

**1.** Set up tagmentation reactions for each plasmid:

  | Component | Concentration | Quantity | 
  | ---------: | ---------: | :---------- |
  | Tagment DNA Buffer | 2X | **10**  µL | 
  |  dsDNA | 0.2 ng/µL | **5**  µL |
  | Amplicon Tagment Mix || **5**  µL |
  || **Total** | **20** µL |
  
  <!-- : in the pipes specify justification -->
  <!-- **X** bolds the inside -->
  
 **2.** In a thermocycler, incubate reactions at 55 °C for 5 minutes, then cool to 10 °C.

**3.** As soon as reactions reach 10 °C, add 5 µL Neutralization Buffer (NT) and incubate 5 min at RT.
  * *Neutralization buffer stops the reaction, so timing is important*
  
**4.** Assemble Nextera PCR reactions:

  | Component | Concentration | Quantity | 
  | ---------: | ---------: | :---------- |
  | Tagmented DNA | | **25**  µL | 
  | i7 index primer | 5µM | **5**  µL |
  | i5 index primer | 5µM | **5**  µL |
  | Nextera PCR Master Mix |3.33X| **15**  µL |
  || **Total** | **50** µL |

<br/><br/><br/><br/><br/>
**5.** Run Nextera PCR:

  | Cycles | Temp | Time | Step |
  | ---------: | :--------: | :---------: |:---------: |
  | **1** | **72 °C** | **3:00** | **enzyme denaturation?** |
  | **1** | **95 °C** | **0:30** | **inital denaturation** |
  
  || 95 °C | 0:10 | denaturation |
  | ---------: | :--------: | :---------: |:---------: |
  | **-12X-** | **55 °C*** | **0:30** | **annealing** |
  || **72 °C** | **0:30** | **extension** |
 
  | 1 | 72 °C | 5:00 | final extension |
  | ---------: | :--------: | :---------: |:---------: |
  

**6.** Clean up PCRs with columns or SPRI beads. Elute libraries in 30 µL of water.
  * Use [SPRI beads](./SPRI-beads.md) to purify (0.65X ratio and 2X washes with 80% ethanol).
  * Alternatively, purify with [column-based kit](https://www.neb.com/-/media/nebus/files/protocols/t1030_quick_protocol_card_monarch_pcrdna_cleanup.pdf?rev=df342b32fb1144af88257b50773a0c7a&hash=662C2FB4EA8277B53B4FE89E3D5887A8)
  
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
