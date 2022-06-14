Printed Circuit board (PCB) settings:

Dimensions  : 99.06mm x 53.34mm
Material    : FR-4 TG130
Layers      : 2
Thickness   : 1.6mm
Solder Mask : Green
Silkscreen  : White
Finish      : HASL/ENIG
Vias        : Tenting vias
Copper      : 1 oz. (All layers) 

List of some manufacturers:
- PCBGoGo
- UET PCB
- SeeedStudio
- JLCPCB

HOW TO ORDER:

Go to one of these manufacturers website, then:

OPTION 1 - FULL ASSEMBLED BOARD (PCBA):

- Select PCBA (PCB + Assembly) option
- Fill PCB settings
- upload Manufacturing_PCBA.zip


OPTION 2 - PCB Only, hand soldering:

- Select PCB option
- Fill PCB settings
- upload Manufacturing_PCB.zip
- buy all components in the BOM_PartType-Vibrotactile BCI shield.xlsx file

these components can be bought from several distributors:
Farnell, RScomponents, Digikey, Mouser, Arrow..


/////////////////////////////////////////////////////////

Updates from initial version:

- Changed software from Altium to Kicad (ver. 6), the reference software used by CNRS (free and open source).
- PCB dimensions reduced to 99.00 x 53.34mm.
- obsolete MOSFET BS170G replaced by BS170
- Motor connectors reference replaced to 282834-2 (smaller footprint, and higher availability)
- Resistors R1 to R12 changed from 6.8 Ohm to 24 Ohm

Motors are rated 3.0V and can go up to 3.7V.
Current at 3.7V is about 55mA
Motors are powered with the 5V rail from the Arduino. Since motors voltage should not exceed 3.7V,
Resistors R1 to R12 values should be:
R = DV / I with:
DV = 5-3.7V = 1.3V 
I = 55mA
Therefore R = 24 Ohm

With this setup all motors can safely be driven by PWM from 0 to 100% dutycycle.

MOTORS:

2 options:

Fast delivery (1-3 days) :
https://www.amazon.fr/0-3in-moteur-vibration-%C3%A9tanche-masseur/dp/B08CHHMVWY/ref=sr_1_4?crid=2JJ113Z7XVKXU&keywords=moteur+vibrant+7mm&qid=1655198366&s=industrial&sprefix=moteur+vibrant+7mm%2Cindustrial%2C63&sr=1-4

Lowest price (1-2 months) : select the 1.5V to 3.7V version
https://fr.aliexpress.com/item/1005002945728204.html?spm=a2g0o.productlist.0.0.43501c7ajrwj7v&algo_pvid=59802b58-b0c1-436a-8371-263ce5a04aeb&algo_exp_id=59802b58-b0c1-436a-8371-263ce5a04aeb-2&pdp_ext_f=%7B%22sku_id%22%3A%2212000022908295436%22%7D&pdp_npi=2%40dis%21EUR%21%212.32%21%21%212.06%21%21%402100bdd716551982956516490e7309%2112000022908295436%21sea

Note: 
Picking 1.5V to 5V motors instead would allow a wider vibration range and remove the need of using resistors R1 to R12.
In this case PCB should be updated to remove the resistors slots.
However these motors have higher price (2.32€ vs 1.07€ for the 3.7V version), and are harder to find for fast delivery.

Note 2:
N-MOSFETs are often facing shortages. 
if BS170 is not available, it can be replaced by one of these references:
2N7000
BS270
VN2106N3-G
VN10KN3-G
2N7008-G
TN2106N3-G
TN5325N3-G
ZVN2110A

