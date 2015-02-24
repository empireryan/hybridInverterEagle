Hybrid Inverter SDP Eagle Rules. Take pride in your work first and foremost.

#File Naming:
- Directory names will be of the form: 'XX' 
- File names are: XX-v10.brd
- Minor versions will be Thingy-v11, v12, v13. Major will be v20, v30.

#PCB Layout:
- Golden Rule ;) 
	*Never mix Analog and Digital Ground. I repeat - Do not cross the streams! We will connect analog and digital grounds
	in one place only on the final board, using an R0 0805 jumper. Digital grounds should be named DGND, analog grounds should be named AGND.	

	*All VCC, 5V, 3.3V, etc will use appropriate power symbol. Naming conventon will be 3V3 for 3.3V, 1V8 for 1.8V, etc...
	Please make sure to change the values of supply symbols to reflect this nameing/labeling convention.

- Create board frame on 0.05” grid. Make the lower left corner start at 0,0.
- Change line width of the board frame to 0.008”.
- Board frame will be square.
- Change top silkscreen color (tPlace) to gray. Bottom silk (bPlace) to yellow. And tDocu to dark
yellow.
- Every board should have the name printed on the tDocu layer for ease of merging later on
- Stick parts on 0.05” grid. You may not break this rule unless you have a very good reason.
- Label any LED with it's purpose (power, status, D4, Lock, etc).
- Label any connector: Vin, Port1, Batt, 5-9V, etc.
- Label pins where applicable: TX, Power, +, Charge, etc.
- Label switches and switch states: On, USB, etc.
- When applicable, when adding labels, move vias and avoid having vias go through the
silkscreen. Gold phoenix will bump labels around and make the board look bad if a via goes
through the silk.
- Components will be grouped together (the resistors surrounding a transistor in the schematic
will also be together on the PCB).
- Using the autorouter is approved for prototypes.
- Hand routing and touchup of the autorouter is expected for production boards.
- 0.020” vias are allowed. 15mil is minimum.
- Use 10mil traces on designs where possible. 6-8 mil is acceptable. 5 mil is minimum (Asbolute minimum per OshPark 4 layer).
- Use thicker traces for power lines where applicable. 12mil=100mA max, 16mil=500mA, and so
on.
- Spacing is 8mil between traces and space.
- No blind or buried vias.
- Use straight lines with 45degree corners. Avoid 90degree corners (Wire style 3 is good for this)
- Use a ground pour on top/bottom layers where applicable. Power and Ground planes for center layers will be on layers 2 and 15 respectively.  
- Use a 12mil isolation setting on any ground pour. This will help prevent pours from shorting to
traces.
- Load the 4layer.dru file included in the git repo!
Schematic Layout:
- All parts will be on 0.1” grid.
- All GND connections will use GND symbol. 
- Use dashed gray lines to separate a complex design into various smaller bits (for example,
charge circuit, accelerometer, etc).

#Footprints:
- All footprints need >Name (on tNames layer) and >Value (on tValues layer). Size of both will be 0.016”. If you come across a part on a board that doesn't have this, you must change it and save the library.
- All footprints need silkscreen or tDocu indicators showing mechanical sizes, dimensions, or anything weired about the part.
- Silkscreen within a footprint or board should NOT go over pads or metal that will be exposed (it'll flake off easily).
- Every new footprint and part will have a description containing part information and whether the footprint has been proven.
Panelization:
- When panelizing a design, copy original board, paste it into a new PCB. Use a 0.1” grid, and place copies of board exactly 0.020” in between copies (all sides). No indicators for v-scoring are needed.
- Make sure you are aware of any overhanging parts between copies. A bluetooth module antenna could over-run SMD components on the copy next door.
Assembly Sheet:
- All assembly sheets will be in PDF form
- All assembly sheets will have version number in tValue text below the design 45) Every part will have value next to the component. Text size should be 0.016” 46) LEDs must have color indicated
- Any component not to be populated will have a large 'DNP' label on part.

#Printing Schematics:
- Print to PDF by hitting the PDF button in Eagle print window 49) Make sure 'Rotate' is NOT checked
- Make sure 'Caption' is NOT checked
- Select Sheets : 'All' to print all sheets
- Scale factor 1
