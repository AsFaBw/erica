# GreatFET-Erica
A neighbor for the GreatFET One targeting the 315/433/868/915MHz bands. This neighbour is not a design from GreatScottGadgets. So if it does not work, don't blame GSG but me.
# Name
The arms of the plant erica remind me a bit to antennas. And that is what Erica shall be about. A neighbor with 4 antennas.
# Purpose
Primary purpose of this neighbor is to provide a possibility to do security research within the 315MHz/433MHz/868MHz/915MHz band. Idea is to have in total 4 CC1101 transceivers available. One tuned for 315MHz band, one tuned for 433MHz band, two for 868MHz/915MHz bands. It should be possible to still receive within the 433MHz band with the transceiver that is tuned for 315MHz. Respectively to receive with the 315MHz tuned transceiver within the 433MHz band.
The two transceivers per band are intended for short reaction times between receive and send... ...or disturbing the transmission of the system under analysis while still capturing any data in the air.

This can be useful for analyzing issues in systems that do require but do not care about RF message integrity (example:  https://www.syss.de/fileadmin/dokumente/Publikationen/Advisories/SYSS-2019-004.txt)

THE PURPOSE OF THIS NEIGHBOR IS NOT TO BE A TOOL FOR CRIMINALS!
# PoC
A first version is under development that is build with pre-build, low cost CC1101 transceivers. 
![Alt text](PoC/GreatFETEricaPoCV0_1.png?raw=true "Erica PoC V0.1")
# Improved version
An improved version shall be build without pre-build CC1101 modules - following the TI refernce designs (http://www.ti.com/tool/CC1101EM868-915_REFDES / http://www.ti.com/tool/CC1101EM433_REFDES).
The improved version shall have external antennas to match to frequencies.
![Alt text](ImprovedVersion/ImprovedVersion.png?raw=true "Erica Improved Version")
![Alt text](ImprovedVersion/EarlySchematic.png?raw=true "early schematic")
![Alt text](ImprovedVersion/Improved3D.png?raw=true "early 3D schematic")
# Concept
The 4 CC1101 shall be accessible via SPI interface
To be a friendly neighbor, the SPI shall be selected via I2C (similar to GF-Crocus)

![Alt text](SPIFriendlyNeighbor.jpg?raw=true "SPI select via I2C")
# Status
PoC: PCB arrived...
![Alt text](PoC/PoCPCB.PNG?raw=true "Erica PoC V0.1 PCB")
...components arrived and partly assembled. Unfortunately used wrong footprint for the PCF8574A. Further I ordered a chinese copy that is hearing on 0x20 instead of 0x38 (although the A version is described to hear on 0x38)
![Alt text](PoC/PoCPartlyAssembled.JPG?raw=true "Erica PoC V0.1 PCB stacked")
...basic access to CC1101 SPI interface (controlled by I2C select) working. Especially gating the SPI select with the 1G32 OR gate:
![Alt text](PoC/PoCBurstSingleSPI.png?raw=true "Erica PoC V0.1 PCB stacked")
While the 868MHz modules can be accessed as expected, the 433MHz module's SPI interface does not respond. Investigated and found that the pinout is different than the one I had used for schematic design:-) There are similar looking 433MHz modules on the market, that have slightly different pin assignments. Used the one for pcb design and ordered the other.
Anyhow, the 868MHz modules operation gave me enough confidence to order the "improved" version. It might be intersting to repair the PoC pcb (design V0.2), as it is possible to assemble such a board for ~20Euros.
![Alt text](PoC/PoCFirstAccessI2CSPI.png?raw=true "Erica PoC V0.1 PCB stacked")

# GreatFET
You don't know GreatFET One yet? Have a look to: https://greatscottgadgets.com/greatfet/
