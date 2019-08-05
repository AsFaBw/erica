# GreatFET-Erica
A yet non-offical neighbor for the GreatFET One targeting the 433/868/915MHz bands
# Name
The plant erica reminds me a bit to antennas. And that is what Erica shall be about. A neighbor with 4 antennas.
# Purpose
Primary purpose of this neighbor is to provide a possibility to do security research within the 433MHz/868MHz/915MHz band. Idea is to have in total 4 CC1101 transceivers available. Two tuned for 433MHz band, one for 868MHz(still allowing to monitor or sending in the 915MHz band), one for 915MHz band(still allowing to monitor or sending in the 868MHz band).

THE PURPOSE OF THIS NEIGHBOR IS NOT TO BE A TOOL FOR CRIMINALS!
# PoC
A first version is under development that is build with pre-build, low cost CC1101 transceivers. 
![Alt text](GreatFETEricaPoCV0_1.png?raw=true "GreatFET Erica PoC V0.1")
# Concept
The 4 CC1101 shall be accessible via SPI interface
To be a friendly neighbor, the SPI shall be selected via I2C (similar to GF-Crocus)

![Alt text](SPIFriendlyNeighbor.jpg?raw=true "SPI select via I2C")
# GreatFET
You don't know GreatFET One yet? Have a look to: https://greatscottgadgets.com/greatfet/
