DNase treatment of cellular RNA
================================================================================
Description: Common RNA purification strategies carry over DNA from cells. A DNase step removes this.

Materials:
--------------------------------------------------------------------------------
  * RNA of cellular origin in water 
  * 2U/µl [TURBO DNase](https://www.thermofisher.com/order/catalog/product/AM2238?SID=srch-srp-AM2238#/AM2238)
  * TURBO DNase 10X buffer
  * Magnetic SPRI beads in crowding solution [(Omega BioTek TotalPure NGS](https://www.omegabiotek.com/product/mag-bind-totalpure-ngs/?gclid=CjwKCAiA1eKBBhBZEiwAX3gqlw2-fi_geWTPQcJVkZdR--dL3zrHwdkoLxc-VhABYCzBcpVGy-4v7BoCtjgQAvD_BwE&cn-reloaded=1)
or [AMPure and RNAClean XP beads)](https://www.beckman.com/reagents/genomic/cleanup-and-size-selection)

Equipment Required:
--------------------------------------------------------------------------------
  
  * 37 °C heat block or thermocycler
  * Magnetic separation rack
     
___
Protocol:
--------------------------------------------------------------------------------

**1.** Dilute 10X DNase buffer to 1X in RNA solution.<br/>_Note: 44 µl of RNA + 5 µl of 10X buffer is sufficient for samples with ~10 µg total RNA. <br/>For samples from larger volumes, you might consider doubling the volume (88 + 10)._

**2.** Add 1 µl of TURBO DNase enzyme (per 50 µl reaction), mix well and incubate at room temperature for 15 minutes. _Note: Longer incubations at higher temps promote contaminant-dependent RNA degradation._

**3.** Purify RNA using 1.8X volumes of [SPRI beads](../NGS/SPRI-beads.md), washing 3x in 70% ethanol and eluting in 20-50 µl nuclease-free water.<br/>_Note: If retaining smaller RNAs, purify with [RNA Clean & Concentrator](https://www.zymoresearch.com/products/rna-clean-concentrator-5) instead._ 

Purified RNA can used for standard reverse transcription or [mutational profiling](../Mutational-Profiling/MaP-RT-Marathon.md).

