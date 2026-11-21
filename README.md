<div align="center">

# 🎹 555 Timer Piano

### An 8-key electronic piano built from pure digital electronics: no microcontroller, no code, just a 555 timer.

![Timer](https://img.shields.io/badge/IC-NE555-blue?style=for-the-badge)
![Keys](https://img.shields.io/badge/Keys-8-ff69b4?style=for-the-badge)
![Supply](https://img.shields.io/badge/Supply-5V-red?style=for-the-badge)
![Simulated](https://img.shields.io/badge/Simulated%20in-Tinkercad-orange?style=for-the-badge)
![Level](https://img.shields.io/badge/Level-Beginner%20Friendly-brightgreen?style=for-the-badge)

</div>

---

## 📖 Overview

This project turns a humble **555 timer IC** into a playable **8-key piano**. The 555 runs in **astable mode**, producing a continuous square wave. Each pushbutton connects a **different resistor** into the timing network, which changes the oscillation frequency and therefore the **pitch** you hear from the piezo buzzer.

No Arduino. No code. Just resistors, a capacitor, and one clever chip.

---

## ⚙️ How It Works

```
   Press key ──► selects a resistor ──► changes RC time constant
                                              │
                                              ▼
   Piezo 🔊 ◄── square wave ◄── 555 (astable) ◄┘
```

The oscillation frequency of a 555 in astable mode is:

```
f ≈ 1.44 / ((R_A + 2·R_B) × C)
```

| Symbol | Role in this circuit |
|:------:|----------------------|
| **R_A** | Fixed resistor (**R2 = 6.2 kΩ**) |
| **R_B** | The resistor switched in by the pressed key |
| **C** | **C1 = 100 nF** timing capacitor |

Different key → different **R_B** → different frequency → **different pitch**. 🎶

---

## 🧰 Components

| Ref | Qty | Component |
|:----|:---:|:----------|
| 1 | 1 | Breadboard Mini |
| U1 | 1 | 555 Timer |
| R1, R5 | 2 | 1 kΩ Resistor |
| R2 | 1 | 6.2 kΩ Resistor |
| R3 | 1 | 390 Ω Resistor |
| R4 | 1 | 910 Ω Resistor |
| R6 | 1 | 1.1 kΩ Resistor |
| R7 | 1 | 620 Ω Resistor |
| R8 | 1 | 1.3 kΩ Resistor |
| R9 | 1 | 1.5 kΩ Resistor |
| C1 | 1 | 100 nF Capacitor |
| S1 – S8 | 8 | Pushbutton |
| S9 | 1 | Slide switch (power on/off) |
| PIEZO1 | 1 | Piezo buzzer |
| P1 | 1 | 5 V power supply |

---

## 🔌 Circuit

Built and simulated in **Tinkercad Circuits** on a mini breadboard.

- 🔴 **5 V** from the supply feeds the circuit through the **slide switch (S9)**
- 🎛️ **8 pushbuttons** each connect their own resistor into the timing network
- 🔵 **100 nF capacitor (C1)** sets the timing together with the selected resistor
- 🔊 **Piezo buzzer** is driven by the 555 output (pin 3) and ground

---

## 🎼 Key Map

Frequencies are calculated with `f ≈ 1.44 / ((R_A + 2·R_B) × C)`, using R_A = 6.2 kΩ and C = 100 nF. Keys run from lowest pitch (left) to highest pitch (right).

| Key | Pushbutton | R_B | Frequency (approx.) |
|:---:|:----------:|:---:|:-------------------:|
| 1 | S1 | 1.5 kΩ | 1565 Hz |
| 2 | S2 | 1.3 kΩ | 1636 Hz |
| 3 | S3 | 1.1 kΩ | 1714 Hz |
| 4 | S4 | 1 kΩ | 1756 Hz |
| 5 | S5 | 1 kΩ | 1756 Hz |
| 6 | S6 | 910 Ω | 1796 Hz |
| 7 | S7 | 620 Ω | 1935 Hz |
| 8 | S8 | 390 Ω | 2063 Hz |

> 💡 Real-world values will differ slightly because of component tolerances.

---

## 🚀 Getting Started

1. **Gather** all components from the list above
2. **Place** the 555 timer on the breadboard
3. **Wire** the resistor row, capacitor, and pushbuttons following the circuit diagram
4. **Connect** the piezo buzzer to the 555 output
5. **Flip** the slide switch to power up ⚡
6. **Play!** 🎹

### ▶️ Run it in the simulator

Open the circuit in (https://www.tinkercad.com/things/9Inecua23Gj/editel), start the simulation, and click the buttons.

---

## 🧠 What You'll Learn

- ✅ How the **555 timer** works in astable mode
- ✅ How **RC networks** control frequency
- ✅ The link between **frequency and musical pitch**
- ✅ Building and debugging circuits on a breadboard

---

## 🔮 Future Improvements

- [ ] Tune each resistor to exact musical notes (C major scale)
- [ ] Add a **volume control** with a potentiometer
- [ ] Swap the piezo for a **speaker + amplifier** for richer sound
- [ ] Add **LEDs** that light up per key
- [ ] Design a **PCB** version

---

<div align="center">

</div>
