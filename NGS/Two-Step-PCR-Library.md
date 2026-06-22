2-step PCR amplification of amplicon sequencing libraries
================================================================================
Description: PCR used to amplify cDNA for Mutational profiling, additionally able to add adapters and indices onto any DNA target.

[Go To Step 1 PCR](#step-1-pcr)

[Go To Step 2 PCR](#step-2-pcr)


Materials:
--------------------------------------------------------------------------------
  **Both Steps**
  * 10 mM dNTP mix (each at 10 mM) _Sometimes these are included in the Enzyme Master Mix_
  * Buffer components (5X buffer, DMSO, Enzyme)
  * SPRI beads
  
  **Step 1 PCR**
  * 10 µM each gene-specific forward and reverse MaP primers
  * cDNA template (1 ng/µL OR unpurified product)  
  
  **Step 2 PCR**
  * Purified Step 1 product (1 ng/µL)
  * [In-house index primers](../CWML-primers.csv)
    * In-house index primer F (i7, 5 µM)
    * In-house index primer R (i5, 5 µM)

  
Equipment Required:
--------------------------------------------------------------------------------
  * Thermocycler
  * Magnetic stand


<!-- Use <br/> to go to next page -->
  
Protocol:
--------------------------------------------------------------------------------
### Step 1 PCR

**1.** In 25 µl volumes, mix 1-3 µl of cDNA, 1.25 µL of each primer, and buffer components according to the polymerase chosen:  
  ◦ [Q5 Hot-start Master Mix](https://www.neb.com/protocols/2012/08/30/protocol-for-q5-hot-start-high-fidelity-2x-master-mix-m0494)
  ◦ [Q5 Hot-start Polymerase](https://www.neb.com/protocols/2012/08/30/pcr-using-q5-hot-start-high-fidelity-dna-polymerase-m0493)
  
  _Note: A high-fidelity polymerase is required to accurately capture mutational profile._
  
  
**2.** Incubate samples in thermocycler with the following settings:  

  | Cycles | Temp | Time | Step |
  | ---------: | :--------: | :---------: |:---------: |
  | **1** | **98 °C** | **1:00** | **inital denaturation** |
  
  **Optional Touchdown phase for lowly represented targets in cDNA**<br/>Annealing temp is reduced by 1 degree each cycle. Total cycles (steps 1+2) should not exceed 30.
  || 98 °C | 0:10 | denaturation |
  | ---------: | :--------: | :---------: |:---------: |
  | **variable** | **72->target °C** | **0:30** | **annealing** |
  || **72 °C** | **0:30** | **extension** |
  
  **Standard amplification phase**
  || 98 °C | 0:10 | denaturation |
  | ---------: | :--------: | :---------: |:---------: |
  | **15-20X** | **target °C** | **0:30** | **annealing** |
  | | **72 °C** | **0:30** | **extension** |
 
  | 1 | 72 °C | 2 minutes | final extension |
  | ---------: | :--------: | :---------: |:---------: |
  
  _Note: Extension time and annealing temp can be optimized for amplicon length and primer Tm._
<!-- The text below creates dropdown lists for links to next steps or hyperlinks -->

**3.** Clean up 1st step PCR with a 1X ratio of [SPRI beads](./SPRI-beads.md), 2x 80% Ethanol washes, and 15 µL elution.

<br/><br/><br/>

### Step 2 PCR

**4.** In 50 µl PCR reactions, mix 2 ng of step 1 product and 5 µL of each index primer. Cycle as follows:

  | Cycles | Temp | Time | Step |
  | ---------: | :--------: | :---------: |:---------: |
  | **1** | **98 °C** | **1:00** | **inital denaturation** |
  
  || 98 °C | 0:10 | denaturation |
  | ---------: | :--------: | :---------: |:---------: |
  | **10X** | **67 °C** | **0:30** | **annealing** |
  | | **72 °C** | **0:30** | **extension** |
 
  | 1 | 72 °C | 2 minutes | final extension |
  | ---------: | :--------: | :---------: |:---------: |

**5.** Clean up 2nd step PCR with a 0.8X ratio of [SPRI beads](./SPRI-beads.md), 2x 80% Ethanol washes, and 15 µL elution.
