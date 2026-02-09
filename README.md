# Cruise-Control-System-Using-PID
MATLAB based cruise control system using PID controller
# Cruise Control System of a Vehicle Using PID Controller

## Project Overview
This project presents a **MATLAB/Simulink-based simulation of a Cruise Control System** for a vehicle using a **PID controller**.  
The system is designed to automatically maintain a constant vehicle speed set by the driver (75 km/h), thereby improving **driving comfort, speed regulation, and fuel efficiency**.

This is a **prototype and simulation-based academic mini project**, developed as part of the **Control Systems Engineering Laboratory**.

---

## Motivation
During long-distance driving, continuously controlling the accelerator can cause driver fatigue and inefficient fuel usage.  
Cruise control systems solve this problem by automatically regulating vehicle speed using feedback control techniques.  
This project demonstrates how **classical control theory (PID control)** can be effectively applied to automotive systems.

---

## System Description
The cruise control system operates as a **closed-loop feedback system**:

1. The driver sets a desired speed.
2. The actual vehicle speed is continuously measured.
3. The error between desired and actual speed is calculated.
4. A PID controller generates the required throttle input.
5. The vehicle dynamics respond and adjust the speed accordingly.

---

## Mathematical Modelling
The vehicle model is derived using **Newton’s Second Law of Motion**.

### Forces acting on the vehicle:
- Engine force \( F_e \)
- Drag force \( F_d \)
- Normal force \( N \)
- Gravitational force \( mg \)

Assuming motion on a flat road:

\[
F_e - F_d = ma
\]

Where:
- \( F_e = k_1 \times \text{throttle input} \)
- \( F_d = k_2 \times v \)

Substituting and simplifying:

\[
\frac{dv}{dt} = -\frac{k_2}{m}v + \frac{k_1}{m}(\text{input})
\]

This equation represents the **plant model** used in the Simulink simulation.

---

## Free Body Diagram and Assumptions
The free body diagram illustrates all forces acting on the vehicle.

### Assumptions:
- Vehicle moves on a flat road (zero slope)
- Drag force is proportional to velocity (Stoke’s law)
- Rolling resistance is neglected
- Vehicle mass remains constant

These assumptions simplify the analysis while maintaining realistic system behavior.

---

## Control Strategy – PID Controller
A **PID controller** is used to regulate vehicle speed:

- **Proportional (P):** Reduces present speed error
- **Integral (I):** Eliminates steady-state error
- **Derivative (D):** Improves stability and reduces overshoot

The PID controller ensures smooth and accurate speed tracking even under disturbances.

---

## MATLAB Simulink Implementation
The cruise control system is implemented in **MATLAB Simulink** as a closed-loop system.

### Model components:
- Desired speed input (75 km/h)
- Error summation block
- PID controller
- Vehicle dynamics block
- Integrator (1/s)
- Disturbance input
- Feedback loop

### Parameters used:
- Vehicle mass \( m = 1000 \, kg \)
- Engine constant \( k_1 = 2 \)
- Drag coefficient \( k_2 = 100 \)

---

## Simulation Results
The simulation output shows the vehicle speed response over time.

### Observations:
- Vehicle speed reaches the desired value of **75 km/h**
- Initial overshoot is minimal
- System settles quickly
- External disturbances are effectively rejected
- Steady-state error is nearly zero

This confirms that the **PID controller successfully maintains constant vehicle speed**.

---

## Applications
- Automotive cruise control systems
- Adaptive Cruise Control (ACC)
- Advanced Driver Assistance Systems (ADAS)
- Autonomous vehicle speed regulation
- Highway and fleet vehicle management

---

## Future Enhancements
- Integration with Adaptive Cruise Control (ACC)
- Use of radar and camera-based sensors
- AI-based adaptive PID tuning
- Vehicle-to-Vehicle (V2V) communication
- Real-time hardware implementation

---

## Tools and Software Used
- MATLAB  
- Simulink  
- Control Systems Toolbox  

---

## Reference Video
This project is technically inspired by the following educational video, which explains cruise control modeling and PID-based control:

📺 YouTube:  
https://youtu.be/cP7XbaOf8iA

The implementation follows standard control system principles and academic references.

---

## Author
**Jeeva S**  
B.E – Electronics and Communication Engineering  
Panimalar Engineering College, Chennai

---

## Project Contents
- 📘 Project Report (PDF)  
- 📊 Presentation (PPT)  
- 🖼️ Mathematical model, free body diagram, Simulink model, and output plots  

⭐ If you find this project useful, feel free to star the repository!

