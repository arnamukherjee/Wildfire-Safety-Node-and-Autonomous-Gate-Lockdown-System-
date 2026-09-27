# Wildfire-Safety-Node-and-Autonomous-Gate-Lockdown-System-
## 📝 Project Description
The Wildfire Safety Node and Autonomous Gate Lockdown System is a smart edge-based safety system designed to improve the safety of rural evacuation routes during wildfire conditions.Using **temperature, humidity, and wind-speed inputs**, the system continuously monitors the surrounding environmental conditions and calculates a **Simplified Fire Weather Index (FWI)** to estimate the level of wildfire risk.

Unlike systems that depend completely on cloud connectivity, this prototype uses **local Arduino-based processing** for real-time risk detection and automatic safety actions.

The system can automatically activate a road barrier, provide alternate-route guidance, and generate visual and audio warnings when the calculated FWI crosses the predefined risk threshold.

This makes the prototype suitable for **IoT hackathons, disaster-management projects, smart road-safety systems, and future edge-based wildfire monitoring solutions**.

---

## 📌 Project Overview

The **Wildfire Safety Node** is an Arduino-based autonomous road-safety prototype designed to monitor changing environmental conditions during wildfire situations.

The system takes three main inputs:

🔹 **Temperature** → Measured using a DHT22 sensor.  
🔹 **Humidity** → Measured using the DHT22 sensor.  
🔹 **Wind Speed** → Simulated using a potentiometer in the prototype.

These inputs are processed locally by the **Arduino Uno**, which calculates a Simplified FWI value and compares it with a predefined threshold.

The system operates in two conditions:

🔹 **Normal Condition** → Road remains open and the safe indicator stays active.  
🔹 **High-Risk Condition** → Gate lockdown, alternate-route indication, buzzer, and danger LED are activated automatically.

---

## 🎯 Project Objective

The main objective is to demonstrate how a **low-cost autonomous edge device** can monitor environmental conditions and provide an automatic road-safety response during increasing wildfire risk.

The prototype focuses on **early local warning, autonomous gate control, and alternate-route guidance** to support safer evacuation management.

---

## ✨ Key Features

- Real-time temperature and humidity monitoring.
- Wind-speed variation simulation.
- Simplified FWI-based wildfire risk detection.
- Local edge processing using Arduino Uno.
- Automatic road-gate lockdown.
- Servo-controlled alternate-route indication.
- Red LED and buzzer for emergency warning.
- Green LED for normal/safe condition.
- Continuous environmental monitoring.
- Wokwi-based virtual circuit simulation.
- Works locally without requiring internet connectivity.

---

## 🛠️ Hardware & Software

### Hardware

- Arduino Uno
- DHT22 Temperature & Humidity Sensor
- Potentiometer for Wind-Speed Simulation
- Servo Motors × 2
- Buzzer
- Red LED
- Green LED
- Resistors
- Breadboard
- Jumper Wires
- 5V Regulated Power Supply

### Software

- Arduino IDE
- Arduino C/C++
- Wokwi Simulator

---

## 📊 Risk Detection Logic

The prototype uses the following simplified FWI calculation:

**Simplified FWI = ((Temperature × 1.2) + (100 − Humidity) + (Wind Speed × 1.5)) / 3**

A predefined threshold of **75** is used in the prototype.

### 🟢 Normal Condition

When:

**FWI < 75**

- Green LED → ON
- Red LED → OFF
- Gate → Open
- Direction Sign → Normal position
- Buzzer → OFF

### 🔴 High-Risk Condition

When:

**FWI ≥ 75**

- Green LED → OFF
- Red LED → ON
- Gate → Closed
- Direction Sign → Alternate route
- Buzzer → ON

> **Note:** The FWI used here is a simplified prototype risk index and is not the official Canadian Fire Weather Index calculation.

---

## ⚙️ How the System Works

The system follows a continuous monitoring and response cycle:

**Temperature + Humidity + Wind Speed**

↓

**Arduino Uno**

↓

**Simplified FWI Calculation**

↓

**Risk Threshold Check**

↓

**Normal Condition / High-Risk Condition**

↓

**Automatic Safety Response**

In a high-risk condition, the Arduino automatically controls the **gate servo, directional-sign servo, red LED, and buzzer**.

---

## 🚧 Autonomous Safety Response

When the calculated FWI reaches the predefined threshold:

🔴 **Danger LED** → Turns ON  
🔊 **Buzzer** → Activates emergency warning  
🚧 **Gate Servo** → Moves to close the road  
↪️ **Sign Servo** → Indicates an alternate route

When the environmental risk falls below the threshold, the system can return to the normal state.

---

## 🔗 Wokwi Simulation

🔗 **Wokwi Project:**  
[View Wokwi Simulation](https://wokwi.com/projects/476312385602555905)
## Circuit Diagram---

<img width="428" height="392" alt="image" src="https://github.com/user-attachments/assets/7b79ef70-8200-4dd0-821c-d594b02354b3" />




The complete prototype is simulated in Wokwi to test the sensor inputs, FWI calculation, servo movement, LEDs, and emergency alert system.

---

## 📈 SWOT Analysis

### Strengths

- Local decision-making without internet dependency.
- Automatic response to increasing wildfire risk.
- Low-cost prototype using easily available components.
- Combines environmental monitoring with road-safety control.
- Can be deployed as multiple roadside safety nodes in future.

### Weaknesses

- Prototype uses simulated wind-speed input.
- Simplified FWI calculation is not a complete wildfire prediction model.
- Sensor accuracy may be affected by extreme environmental conditions.
- Prototype components are not designed for direct outdoor deployment.

### Opportunities

- Deploy multiple nodes along wildfire-prone roads.
- Integrate real wind-speed and weather sensors.
- Add solar power and battery backup.
- Develop a centralized emergency monitoring dashboard.
- Integrate real-time weather and wildfire data.
- Extend the system for smart disaster-management networks.

### Threats

- Extreme heat, smoke, and weather may affect electronic components.
- Sensor failure can affect risk estimation.
- Communication or power failures may affect connected versions.
- Real-world deployment requires ruggedized and properly tested hardware.

---

## 🔮 Future Development

- Replace the potentiometer with a real **anemometer** for wind-speed measurement.
- Use more accurate weather and fire-risk sensors.
- Add **solar power with battery backup**.
- Develop weatherproof outdoor enclosures.
- Deploy multiple interconnected safety nodes.
- Add cloud/mobile dashboard for remote monitoring.
- Integrate real-time weather and wildfire data.
- Improve the risk model using historical and real-world environmental data.
- Add additional emergency communication mechanisms.

---

## 🧪 Prototype Testing

The prototype can be tested by changing:

- Temperature
- Humidity
- Wind-speed input

As these conditions change, the Arduino recalculates the Simplified FWI and automatically changes the system state.

For example, increasing **temperature and wind speed** while decreasing **humidity** increases the calculated risk value and can trigger the high-risk response.



## 📢 Developed For IoTRICITY-Season 3 Hackathon by Team NodeX
