Pooling and denaturing libraries for sequencing on the MiSeq
================================================================================
Description: DNA must be at a specific molarity range to run on the sequencer

Materials:
--------------------------------------------------------------------------------
  * DNA libraries (1 to 4 nM)
  * phiX library
  * Illumina Sequecing kit
  * 1 N NaOH stock
  * 200 mM Tris-HCl pH 7.0

Equipment Required:
--------------------------------------------------------------------------------
  * Illumina MiSeq
  * Milli-Q water source
  * lens paper
  
___
Protocol:
--------------------------------------------------------------------------------
**Part 0: Thawing the sequencing kit**

_Sequencing kits are best thawed at 4 °C overnight,_<br/>
_but can also be thawed for 2 hours in a room temperature water bath._<br/>
_Save at 4 °C until loading. Don't discard the HT1 buffer that comes with the kit._

**Part 1: Pooling varying sequencing libraries together**<br/>
_Note: Confirm each library fits the chosen kit (300, 500 cycles?) and has no barcode overlap._

**1.** Determine % of kit need for each library.
  * MaP Amplicon libraries that fit the kit cycles require 2 %
  * MaP Nextera libraries from larger sequences need (length/cycles x 2) %
  * Plasmid Nextera libraries need 0.5 %

**2.** Pool like libraries (that need the same %) together to at least 1 nM (4 nM is best).<br/>
_Note: this [form](https://docs.google.com/spreadsheets/d/1Ikx9kMZMRp9ZMFnYnInP_5jzi7-A4LaZf_DpWXz3J_s/edit?usp=share_link) can be used to help with pooling._

**3.** Combine varying libraries until 100 % of a kit is accounted for.<br/>
_Note: combinations of low-diversity libraries should be supplemented with 20-30 % PhiX._

**Part 2: Preparing the sequencer**

**4.** Ensure there is at least 100 GB free space on the "Data" drive of the sequencer.<br/>
When deleting data, permanently delete anything older than 6 months first.

**5.** Prepare the SampleSheet and load onto the instrument.

**6.** Power cycle the instrument.
  * Shut down the system from within the sequencing program
  * Click "Shut down anyway" if necessary to turn off the computer
  * Turn the power switch in the back of the instrument off
  * Wait about 1 minute before turning the power switch back on
  * Sign into the computer, the sequencing software should start

**Part 3: Preparing the flow cell**

**7.** Retrieve the flow cell and rinse 3 times in its container with Milli-Q water.

**8.** Shake off excess water and dry flow cell with lens paper. <br/>
_Note: Goal is to wipe away specks from the lanes._<br/>
_A dab of 100 % EtOH on new lens paper can help clean and dry._

**9.** Set aside flow cell until ready to load.

**Part 4: Denaturing the library pool to 20 pM**

**10.** Dilute a fresh stock of 0.2 N NaOH (200 µL 1 N stock and 800 µL water)

**11.** Mix 5 µL of library pool and 5 µL of 0.2 N NaOH. Vortex mix.<br/>
_Note: Volumes can be increased up to 10/20 µL for 2/1 nM pools (but 4 nM works best)._

**12.** Spin down library at 280 x g for 1 min. Incubate at room temperature for 4 min.

**13.** Quench base with 5 µL of 200 mM Tris-HCl pH 7. Vortex and spin down.<br/>
_Note: Increase volumes to 10/20 µL for 2/1 nM pools._

**13.** Dilute library up to 1 mL with HT1 buffer (985 µL for a quenched 4 nM library).

**Part 5: Adjusting deantured library to final concentration with PhiX**

**14.** Mix library with 20 pM denatured PhiX at desired %.<br/>
_Note: PhiX 20 pM libraries can be prepared as laid out above._

**15.** Dilute library to final concentration.
  * for 9 pM  : 270 µL of library and 330 µL HT1 buffer _(totally safe for amplicons)_
  * for 10 pM : 300 µL of library and 300 µL HT1 buffer _(usually ok but gambling)_
  * for 12 pM : 360 µL of library and 240 µL HT1 buffer _(ok with V3 600 kits)_

**Part 6: Loading the instrument**

**16.** Retrieve the sequencing cartridge. <br/>
Pierce the cartridge port labeled "Load Sample" with a P1000 pipette tip.
Load all 600 µL of your pool into this port with a new tip.

**17.** Open the sequencing software and follow the onscreen prompts:
  * sign into basespace
  * confirm SampleSheet parameters
  * load new flow cell
  * load the wash buffer (remember to put down the sipper)
  * load the cartridge
  * Hit next to see system checks
 
 **18.** While system checks are running, rinse out old wash bottle and tray. <br/>
 _Note:Usually good to rinse out each three times with Milli-Q water._
 
 **Part 7: Post-Run Wash**
 
 **19.** Once sequencing is complete. Replace new filled wash bottle and tray and run wash.
   * Mix 25 mL 10% Tween and 475 mL Milli-Q water in wash bottle
   * Dispense about 6 mL of wash buffer to each port of wash tray
   * Remove formamide-containing fluid from port 8 of used cartridge
   * Dispose of cartridge and waste in waste bottle in appropriate containers
   * Leave the flow cell in the instrument
  
<!-- The text below creates dropdown lists for links to next steps or hyperlinks -->
