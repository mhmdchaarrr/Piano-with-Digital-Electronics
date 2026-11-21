# Piano-with-Digital-Electronics
This project turns a humble 555 timer IC into a playable 8-key piano. The 555 runs in astable mode, producing a continuous square wave. Each pushbutton connects a different resistor into the timing network, which changes the oscillation frequency, and therefore the pitch you hear from the piezo buzzer.

No Arduino. No code. Just resistors, a capacitor, and one clever chip.

⚙️ How It Works

   Press key ──► selects a resistor ──► changes RC time constant
                                              │
                                              ▼
   Piezo 🔊 ◄── square wave ◄── 555 (astable) ◄┘

The 555 oscillation frequency in astable mode is:

f ≈ 1.44 / ((R_A + 2·R_B) × C)

Symbol	Role in this circuit
R_A	Fixed resistor (R2 = 6.2 kΩ)
R_B	The resistor switched in by the pressed key
C	C1 = 100 nF timing capacitor

Different key → different R_B → different frequency → different note. 🎶

🧰 Components

Ref	Qty	Component
1	1	Breadboard Mini
U1	1	555 Timer
R1, R5	2	1 kΩ Resistor
R2	1	6.2 kΩ Resistor
R3	1	390 Ω Resistor
R4	1	910 Ω Resistor
R6	1	1.1 kΩ Resistor
R7	1	620 Ω Resistor
R8	1	1.3 kΩ Resistor
R9	1	1.5 kΩ Resistor
C1	1	100 nF Capacitor
S1 – S8	8	Pushbutton
S9	1	Slide switch (power on/off)
PIEZO1	1	Piezo buzzer
P1	1	5 V power supply

🔌 Circuit

📸 Add your schematic image here:
![Circuit Diagram](images/circuit.png)

Quick wiring summary

	•	🔴 5 V from the supply feeds the 555 through the slide switch (S9)
	•	🎛️ 8 pushbuttons each connect their own resistor into the timing network
	•	🔵 100 nF capacitor sets the timing together with the selected resistor
	•	🔊 Piezo buzzer connects to the 555 output (pin 3) and ground

🎼 Key Map

Fill in the measured frequency and note for your build:

Key	Pushbutton	Resistor	Frequency	Note
1	S1			
2	S2			
3	S3			
4	S4			
5	S5			
6	S6			
7	S7			
8	S8			

🚀 Getting Started

	1.	Gather all components from the list above
	2.	Place the 555 timer on the breadboard
	3.	Wire the resistor row, capacitor, and pushbuttons following the circuit diagram
	4.	Connect the piezo buzzer to the 555 output
	5.	Flip the slide switch to power up ⚡
	6.	Play! 🎹

▶️ Run it in the simulator

Open the circuit in Tinkercad Circuits, start the simulation, and click the buttons.

🧠 What You'll Learn

	•	✅ How the 555 timer works in astable mode
	•	✅ How RC networks control frequency
	•	✅ The link between frequency and musical pitch
	•	✅ Building and debugging circuits on a breadboard

🔮 Future Improvements

	☐︎	Tune each resistor to exact musical notes (C major scale)
	☐︎	Add a volume control with a potentiometer
	☐︎	Swap the piezo for a speaker + amplifier for richer sound
	☐︎	Add LEDs that light up per key
	☐︎	Design a PCB version

👤 Author

Your Name
📧 your.email@example.com · 🔗 GitHub
