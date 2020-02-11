Board Description
-----------------

board designation           : LimeSDR_Mini_1v3
board version		        : v1.3
board type                  : Lead Free
board size                  : 69 mm x 31.38 mm
panel size					: 89.4 mm x 170.68 mm
panel type					: Vscore + mill cutouts
board thickness             : 1.6 mm +/- 10 %
board material              : IT-180A
number of layers            : 8 (6 inner)
 

Top layer copper foil thickness: 17.5 um
Dielectric thickness between Top layer and 2nd layer: 173 um (6.8 mils)
Dielectric between Top layer and 2nd layer relative permittivity (Er): 4.2

Bottom layer copper foil thickness: 17.5 um
Dielectric thickness between L11 layer and Bottom layer: 173 um (6.8 mils)
Dielectric between L11 and Bottom layer relative permittivity (Er): 4.2


minimum finished hole size  :  200 um
minimum spacing             :  100 um
minimum track width         :  100 um

drill diameters             : finished hole

plating finish (both sides) : immersion gold
                              0.05-0.10 um of gold over
                              2.50-5.00 um of nickel
							
Top silkscreen              : Required
Bottom silkscreen           : Required



Drill files
-----------------
	- LimeSDR_Mini_1v3_panel.DRR -> Drill report detailing the tool assignments, hole sizes, hole count and tool travel. 
   
	- Throughole vias are covered in the following files:
   								File Name																	Start Layer						Stop Layer
						LimeSDR_Mini_1v3_panel-RoundHoles.TXT													Top								Bottom
	- Slotholes are covered in the following files:
						LimeSDR_Mini_1v3_panel-SlotHoles.TXT													Top								Bottom	
						
	- IMPORTANT! Hole diameters are final manufactured diameters INCLUDING HOLE METALIZATION.
	
Gerber files
---------------

			File Name					Layer/Comment
		LimeSDR_Mini_1v3_panel.GTL				Top (RF/Signal/GND)
		LimeSDR_Mini_1v3_panel.G1				L2  (GND)
		LimeSDR_Mini_1v3_panel.G2				L3  (PWR/GND)
		LimeSDR_Mini_1v3_panel.G3				L4  (Signal/PWR/GND)
		LimeSDR_Mini_1v3_panel.G4				L5  (Signal/PWR/GND)
		LimeSDR_Mini_1v3_panel.G5				L6  (CLK/Signal/GND)
		LimeSDR_Mini_1v3_panel.G6				L7  (GND)	
		LimeSDR_Mini_1v3_panel.GBL				Bottom (Signal/PWR/GND)

		 
		LimeSDR_Mini_1v3_panel.GPB				Bottom Pad Master
		LimeSDR_Mini_1v3_panel.GPT				Top Pad Master

		LimeSDR_Mini_1v3_panel.GTO				Top Overlay
		LimeSDR_Mini_1v3_panel.GTP				Top Paste
		LimeSDR_Mini_1v3_panel.GTS				Top Solder

 
		LimeSDR_Mini_1v3_panel.GBS				Bottom Solder
		LimeSDR_Mini_1v3_panel.GBP				Bottom Paste
		LimeSDR_Mini_1v3_panel.GBO				Bottom Overlay


		LimeSDR_Mini_1v3_panel.GM1				Mechanical 1 (Board Cutout)


		LimeSDR_Mini_1v3_panel.GM14				ASM BOT (Assembly bottom)
		LimeSDR_Mini_1v3_panel.GM15				ASM TOP (Assembly top)
		
  
Important Notes
---------------
All 0.2mm vias including 0.35mm ring and 0.2mm drill via-in-pads must be resin filled with metal cap (IC1).

IC1 thermal pad vias with 0.4mm ring and 0.2mm drill must be resin filled with metal cap.

IC1 thermal pad vias with 0.5mm ring and 0.2mm drill must be left open (NO resin fill with metal cap). 4 vias in total, marked with note in mechanical 1 (*.GM1) gerber file.

DRCs must be run on Gerber files before building boards.

All through hole vias may be plated shut.

Solder mask : dark blue, both sides, halogen free, glossy finish (NOT matte).

Silkscreen : white epoxy ink, halogen free, both sides. No silkscreen on pads.

Electrical test : 100 % netlist.

Boards are to be individually bagged.

Design software used : Altium Designer 19.1.5 (build 86)

Controlled Impedance
--------------------
	
  * 50 Ohm microstrip line (Top layer, RF) characteristics:
    Top layer copper foil thickness: 17.5 um
	Track width = 0.309 mm (12.16 mils)
	Track width/spacing ratio = 1.786
	Dielectric thickness from top to L2 = 173um (6.8 mils)
	Dielectric between Top layer and 2nd layer relative permittivity (Er): 4.2
	
	Approximate microstrip line impedance = 49.9998 Ohms (+/- 10% tolerance)

  * 100 Ohm coupled microstrip line (Top layer, RF) characteristics:
    Top layer copper foil thickness: 17.5 um
	Track width = 0.2 mm (7.87 mils)
	Track spacing = 0.14 mm (5.51 mils)
	Track width/spacing ratio = 1.428
	Dielectric thickness from top to L2 = 173um (6.8 mils)
	Dielectric between Top layer and 2nd layer relative permittivity (Er): 4.2
	
	Approximate coupled microstrip line impedance = 100.752 Ohms (+/- 10% tolerance)
	
  * 90 Ohm coupled microstrip line (Top layer, USB3) characteristics:
    Top layer copper foil thickness: 17.5 um
	Track width = 0.2 mm (7.87 mils)
	Track spacing = 0.1 mm (3.93 mils)
	Track width/spacing ratio = 2
	Dielectric thickness from Top to 2nd layer = 173um (6.8 mils)
	Dielectric between Top layer and 2nd layer relative permittivity (Er): 4.2
	
	Approximate coupled microstrip line impedance = 90.5 Ohms (+/- 10% tolerance)	
	
  * 90 Ohm coupled microstrip line (Bottom layer, USB3) characteristics:
    Bottom layer copper foil thickness: 17.5 um
	Track width = 0.2 mm (7.87 mils)
	Track spacing = 0.1 mm (3.93 mils)
	Track width/spacing ratio = 2
	Dielectric thickness from L11 to Bottom layer = 173um (6.8 mils)
	Dielectric between L11 layer and Bottom layer relative permittivity (Er): 4.2
	
	Approximate coupled microstrip line impedance = 90.5 Ohms (+/- 10% tolerance)