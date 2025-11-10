Mutational profiling (MaP) with SuperScript II
================================================================================
Description: Mn<sup>2+</sup> in buffer encourages transcriptase read-through of modified nucleotides.<br/>
Mutations and deletions at sites of read-through can be mapped by sequencing.

Before starting:
--------------------------------------------------------------------------------
* [In-cell crosslinking with SDA](../Chemical-Probing/SDA-Xlinking.md)
* [OOPS RNP enrichment](../Chemical-Probing/OOPS-RNP.md)
* [*In Vitro* SHAPE RNA profiling](../Chemical-Probing/In-Vitro-SHAPE.md)

Materials:
--------------------------------------------------------------------------------
  * **Modified RNA** _(and unmodified for control)_
    * 5 pmoles of _in vitro_ RNA transcript,
    * 0.5-5 µg of cellular RNA (depending on representation of RNA of interest), **OR**
    * enriched target RNA
  * **2 µM of gene specific primer (_targeted_) or 70 µM (200 ng/µL) of [random nonamer](https://www.neb.com/products/s1254-random-primer-9#Product%20Information) (_for non-targeted_)**
  * **10 mM dNTPs**
  * **10X NTP minus buffer** _(make fresh and keep on ice)_  
    ◦ 500 mM Tris pH 8.0  
    ◦ 750 mM KCl  
    ◦ 100 mM DTT _(Note: Don't use DTT that has been freeze-thawed more than once.)_  
  * [**5M Betaine**](https://www.fishersci.ca/shop/products/betaine-5m-solution-molecular-biology-grade-ultrapure-affymetrix-usb-3/aaj77507ucr)
  * **40 mM MnCl<sub>2</sub>**  
  * **200 U/µl** [**SuperScript II**](https://www.thermofisher.com/order/catalog/product/18064022#/18064022) **Reverse Transcriptase**
  * [**G-50 microspin columns**](https://www.cytivalifesciences.com/en/us/shop/molecular-biology/purification/gel-filtration-columns/illustra-microspin-g-50-columns-p-00056)
 _(for lowly expressed targets and randomer-primed samples)_  
  
Equipment Required:
--------------------------------------------------------------------------------
  * Thermocycler

___
Protocol:
--------------------------------------------------------------------------------

**1.** For each sample, combine 7 µl RNA, 1 µl primer, and 2 µl of dNTPs. <br/>Denature at 68-75 °C for 5 minutes, then anneal on ice for 2 minutes.

**2.** Assemble enough RT master mix for each sample, adding manganese only immediately before use:

  | Component | Concentration | Quantity | 
  | ---------: | ---------: | :---------- |
  | NTP minus buffer | 10X | **2**  µL | 
  | Betaine | 5M | **4**  µL |
  | MnCl<sub>2</sub> | 40 mM | **3**  µL |
  || **Total** | **9** µL |
  
  **The color should change upon adding MnCl<sub>2</sub>. If it doesn't, you need new NTP minus buffer.**  
  _Note: You can lower the volume (increase concentration) of MnCl<sub>2</sub> to 0.5 µL to accomodate larger RNA volumes._
  
**3.** Mix 9 µL of master mix with 10 µL of each primer-RNA mix and incubate for 2 minutes at 25 °C. 

**4.** Add 1 µL of SSII RT enzyme to each reaction and perform the following thermocycles:

  | Step | Temp | Time | Action |
  | ---------: | :--------: | :---------: |:---------: |
  | **i** | **25 °C** | **10:00** | **Equilibration** |
  | **ii** | **42 °C** | **90:00** | **Extension** |
  
  **Cycle 10 times**  
  | iiia | 50 °C | 2:00 ||
  | ---------: | :--------: | :---------: |:---------: |
  | **iiib** | **42 °C** | **2:00** | **Extension past difficult adducts** |
 
  **End Reaction** 
  | iv | 70 °C | 10:00 | Enzyme denaturation |
  | ---------: | :--------: | :---------: |:---------: |

**5.** cDNA product purification:  
  ◦ For abundant targets, product cDNA can go straight into PCR amplification.  
  ◦ For lowly expressed targets and randomly-primed reactions, buffer exchange with [G50 columns](../NGS/G-50-microspin.md).

**(6.)** Dilute randomly-primed cDNA to 34 µL in preparation for second-strand synthesis.
  
<!-- The text below creates dropdown lists for links to next steps or hyperlinks -->

<details>
  <summary>Next Steps</summary>
  
</p> <a href="../NGS/Second-Strand-Synthesis.md">
Second-Strand Synthesis</a>

</p> <a href="../NGS/Two-Step-PCR-Library.md">
2-step PCR library generation </a>

</details>

<details>
  <summary>More Info</summary>
  
  <a href="https://doi.org/10.1038/nprot.2015.103">
Original SHAPE-MaP Protocol</a>  

</details>
