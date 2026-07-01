# 🌞 LDR (Light Dependent Resistor) Circuit with Arduino UNO

### Made by **Sir Anwar Siraj – DS & AI Robotics**

---

# 📖 Introduction

This project demonstrates how to interface an **LDR (Light Dependent Resistor)** with an **Arduino UNO**. The LDR detects the surrounding light intensity and sends an analog signal to the Arduino through pin **A0**. The Arduino continuously reads the light level and controls the **built-in LED on Pin 13**.

When the surrounding environment becomes dark, the LED turns **ON**. When the light intensity increases, the LED turns **OFF**.

---

# 💡 What is an LDR?

An **LDR (Light Dependent Resistor)**, also called a **Photoresistor**, is a light-sensitive electronic component. Its resistance changes according to the amount of light falling on its surface.

- 🌑 In darkness → Resistance is very high.
- ☀️ In bright light → Resistance becomes very low.

Because of this property, an LDR is widely used as a light sensor in electronic and Arduino projects.

---

# ⚙️ Working Principle

The LDR works on the principle of **Photoconductivity**.

When light falls on the surface of the LDR, photons excite electrons inside the semiconductor material. This increases conductivity and decreases the resistance of the LDR.

- More Light → Lower Resistance
- Less Light → Higher Resistance

The Arduino measures this change as an analog voltage and makes decisions based on the programmed threshold value.

---

# 🔌 Circuit Description

The circuit consists of:

- Arduino UNO
- LDR (Light Dependent Resistor)
- 10kΩ Resistor
- Breadboard
- Jumper Wires

The LDR and the 10kΩ resistor form a **Voltage Divider**.

### Connections

| Component | Arduino Pin |
|-----------|-------------|
| LDR | 5V |
| Junction of LDR & 10kΩ | A0 |
| 10kΩ Resistor | GND |
| Built-in LED | Pin 13 |

---

# 🔄 How the Circuit Works

### Step 1

The Arduino supplies **5V** to the LDR.

### Step 2

The LDR changes its resistance according to the amount of light.

### Step 3

The LDR and the 10kΩ resistor create a voltage divider.

### Step 4

Arduino reads the voltage at **Analog Pin A0**.

```cpp
int data = analogRead(A0);
```

### Step 5

The sensor value is compared with the threshold value.

```cpp
if(data <= 70)
```

### Step 6

If the sensor value is **70 or below**, it indicates darkness and the built-in LED turns ON.

```cpp
digitalWrite(13, HIGH);
```

### Step 7

If the sensor value is **greater than 70**, the environment is bright and the LED turns OFF.

```cpp
digitalWrite(13, LOW);
```

---

# 📊 Circuit Operation

### Dark Condition

- LDR Resistance = High
- Arduino Value = Low
- LED = ON

### Bright Condition

- LDR Resistance = Low
- Arduino Value = High
- LED = OFF

---

# 📌 Components Required

- Arduino UNO
- LDR (Photoresistor)
- 10kΩ Resistor
- Breadboard
- Jumper Wires
- USB Cable

---

# 🚀 Applications

- Automatic Street Light System
- Smart Home Lighting
- Day and Night Detection
- Solar Garden Lights
- Security Alarm Systems
- Automatic Brightness Control
- Arduino Learning Projects
- Robotics Projects
- IoT Light Monitoring Systems

---

# 🎯 Advantages

- Simple Circuit
- Low Cost
- Easy to Build
- Beginner Friendly
- Low Power Consumption
- Reliable Light Detection

---

# 📚 Learning Outcomes

After completing this project, you will learn:

- What an LDR is.
- How an LDR works.
- Voltage Divider Concept.
- Reading Analog Sensors with Arduino.
- Using `analogRead()`.
- Using `if-else` statements.
- Controlling the Built-in LED.
- Creating simple light automation projects.

---

# 🖼️ Circuit Diagram

Add your circuit diagram image here.

```markdown
![LDR Circuit Diagram](CIRCUIT%20DIAGRAM.png)
```

---

# 💻 Arduino Code

Upload your Arduino sketch file and include it like this:

```markdown
[LDR Arduino Code](LDR_Circuit.ino)
```

---

# 🏆 Project Summary

This Arduino project uses an **LDR (Light Dependent Resistor)** to detect ambient light. The LDR and a **10kΩ resistor** create a voltage divider whose output is connected to **Analog Pin A0**. The Arduino continuously reads the analog value and compares it with a threshold. When the environment is dark, the built-in LED connected to **Pin 13** turns ON. When the environment becomes bright, the LED turns OFF. This project is an excellent introduction to analog sensors, voltage dividers, and basic automation using Arduino.

---

## 👨‍🏫 Made By

# **Sir Anwar Siraj**
### DS & AI Robotics
