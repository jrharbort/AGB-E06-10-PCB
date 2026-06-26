### PLEASE READ EVERYTHING!!

This project is a recreation of the AGB-E06-10 PCB used in some early Nintendo Game Boy Advance titles. Its purpose is to be used as a game repair PCB and is also compatible with parts from AGB-E06-01 revision boards, but it is not compatible as a replacement for AGB-E06-20 boards.

While the E06-01/E06-10 boards were not used on many games, they were used on several early and notable titles. These include:

**Castlevania - Circle of the Moon** (Castlevania in EU)

**F-Zero - Maximum Velocity** (USA and EU)

**Megaman - Battle Network** (EU)

**Wario Land 4** (USA and EU)

Considering no known "junk" games used this revision board, the only viable way to repair these games with a new board was to dismantle another desireable game. Not ideal. This is why I took on the task of creating this repair board. I recreated the board by hand in KiCad and used high resolution scans found on [Internet Archive](https://archive.org/details/agb-e-06-10) as a reference.

This board is fully open source, all KiCad and Gerbers are being made freely available. I do not own anything related or take credit for the design, as that is original property of Nintendo. However, if you found this project useful you can feel free to tip me on [**Ko-Fi**](https://ko-fi.com/jrharbort).

### How to get these boards
You can download either the Gerber or KiCad files from this project and upload them to be fabricated at the PCB fab of your choice. I recommend using the following settings for fabrication. **IF YOU DO NOT SELECT THESE OPTIONS, YOUR BOARDS WILL NOT FIT OR WORK AS EXPECTED!**
* Thickness: 0.8mm
* Surface Finish: ENIG/Immersion Gold
* Castellated Holes: No
* Copper Weight: Both 1oz or 2oz will work fine.

### Materials
This is a bill of materials taken from a copy of Castlevania - Circle of the Moon. Should you lose a capacitor or resistor, you can use this as a reference to get the parts from sites like Mouser or Digikey. I recommend X7R grade components as replacements.

| Reference | Part | Description | Type |
|-|-|-|-|
| U1 | Original ROM | The 44-pin ROM chip on the right, get from original Cartridge. | TSOP-44 |
| U2 | SRAM | 32KB/256Kbit 28-pin SRAM. Obtain from original cartridge or a junk cart. | SOIC-28 |
| U3 | BU9803F | Power Supervisor IC. Obtain from original cartridge. | SOIC-8 |
| U4 | PST3425 | System Reset IC, get from original cartridge. | SOT-25 |
| C1, C2, C3, C6 | CGA2B2X7R1C154K050BA | 0.15uF Capacitor | 0402 |
| C4 | CL05B104KO3LNNC | 0.1uF capacitor | 0402 |
| C5 | N/A | Not populated | 0603 |
| R1 | ERJ-2RKF1001X | 1k Ω Resistor | 0402 |
| R2,R4 | RC0402FR-7D100KL | 100K Ω Resistor | 0402 |
| R3 | RC0402FR-075KL | 5K Ω Resistor | 0402 |
| BT1 | CR-1616/F2N | Tabbed CR1616 available online from various stores. | Tabbed CR1616 |

## Front
<img width="2007" height="1215" alt="E06-10-Front" src="https://github.com/user-attachments/assets/492f5362-102c-4962-a07c-c7ebd4ca9a69" />

## Back
<img width="2005" height="1215" alt="E06-10-Back" src="https://github.com/user-attachments/assets/9c56c357-075d-4010-a9d3-40e8438f2c98" />


### Credits
Special thanks to [AchillesPDX](https://github.com/achillespdx) for assistance in verifying some traces in this board design and testing SMD values, completing this project would have been far more difficult without their help.

### Changes
Rev 1.2
- Corrected missing connection from VIAs to SRAM pins 24 & 25. Previous revisions will require a wire jump from SRAM pin 25 to ROM pin 28, and SRAM pin 24 to ROM pin 29.

### Changes
Rev 1.1
- Small change made to edge connector Pin 6. Any boards printed with Rev 1.0 should not see any functional issues.

Rev 1.0
- This is the first revision. Everything should be working as intended if you select the correct options for fabrication. If you encounter any issues please let me know.
