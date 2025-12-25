# Automatic Door Locking Password System using Arduino UNO, LCD 16 x 2 (I2C) and Micro Servo Motor

##  Introduction
This project is a **simple yet functional Arduino-based password-controlled door lock system** implemented using a **4×4 matrix keypad**, **16×2 I2C LCD**, and a **micro servo motor**. The system allows a user to enter a predefined 4-character numeric password using the keypad. If the password is correct, the servo motor actuates to simulate automatic door opening; otherwise, access is denied.

This simulation-based prototype was created as a **beginner-level embedded systems project** and serves as an introduction to **keypad interfacing, I2C communication, servo control, and basic access control logic**.

---

##  Project Objectives
- Implement a password-based door access system using Arduino  
- Interface a 4×4 keypad for user input  
- Display system status on a 16×2 I2C LCD  
- Control a servo motor to simulate door opening and closing  
- Build a simple and understandable embedded security prototype  

---

##  Key Features
- 4-character password authentication  
- Masked password entry using `*` characters  
- LCD feedback for user interaction  
- Servo-based automatic door opening and closing  
- Reset and retry functionality  
- Simple and beginner-friendly logic  

---

##  System Overview
The system operates based on user input from the keypad and follows a conditional decision-making process:

1. User enters a 4-digit password using the keypad  
2. Input is masked and displayed as `****` on the LCD  
3. On pressing **`D` (Enter key)**, the password is verified  
4. If correct → Servo rotates to open the door  
5. If incorrect → Error message is displayed  
6. Press **`C`** to close the door after opening  

---

##  Hardware Components Used
| Component | Description |
|--------|------------|
| Arduino Uno | Main microcontroller |
| 4×4 Matrix Keypad | User input interface |
| 16×2 I2C LCD (MCP23008) | Displays system messages |
| Micro Servo Motor | Simulates door locking mechanism |
| Jumper Wires | Circuit connections |
| USB / External Power | System power supply |

---

##  Software & Libraries Used
- **Arduino IDE** – Code development and uploading  
- **Keypad.h** – Keypad scanning and input handling  
- **Servo.h** – Servo motor control  
- **Wire.h** – I2C communication  
- **Adafruit_LiquidCrystal.h** – LCD control (used for MCP23008-based I2C LCD at address `0x20`)  

>  Note: The LCD used in this simulation is based on the **MCP23008 I2C expander (address 0x20 / 32)**, which is why the `Adafruit_LiquidCrystal` library is required instead of the commonly used `LiquidCrystal_I2C` library.

---

##  Working Principle
- The keypad is continuously scanned for key presses.
- Numeric keys (`0–9`) are stored as password input.
- The LCD displays masked input (`*`) for security.
- Pressing **`D`** acts as the **Enter key**.
- If the password matches (`1234`), the servo rotates to **90°** (door open).
- Pressing **`C`** closes the door by returning the servo to **0°**.
- Pressing **`#`** resets the current password entry.

---

##  Simulation
The complete circuit and code were simulated using **TinkerCAD Circuits**, including:
- Keypad input validation  
- LCD I2C communication  
- Servo actuation  
- Password logic testing  

---

##  Applications
- Basic electronic door lock systems  
- Smart lockers  
- Home automation prototypes  
- Educational embedded systems projects  
- Password-based access control demonstrations  

---

##  Usage Instructions
1. Power the Arduino system  
2. Enter the 4-digit password using the keypad  
3. Press **`D`** to submit the password  
4. If correct → Door opens  
5. Press **`C`** to close the door  
6. Press **`#`** to reset password entry  

---

##  References & Credits
- Inspired by **Ouasil Technology (YouTube)**  
- Arduino Official Documentation  
- Adafruit LCD Library Documentation  
- TinkerCAD Circuits  

---

##  Author
**Soureen Majumder**  
Instrumentation and Electronics Engineering Student  
GitHub: `@Soureen25`

---

##  Acknowledgements
This project marks my **first GitHub repository** and is developed purely for learning and demonstration purposes. Special thanks to **Ouasil Technology** for the inspiration and to the open-source Arduino community.

---

###  Notes
- This is a **prototype-level simulation**, not intended for real-world security use.
- The key **`D` acts as the Enter key** and must be pressed after entering the password.

https://www.tinkercad.com/things/ePbtsoYaDYD-auto-door-pwd/editel?returnTo=https%3A%2F%2Fwww.tinkercad.com%2Fdashboard%2Fdesigns%2Fcircuits

<img width="1917" height="893" alt="Screenshot 2025-07-30 022932" src="https://github.com/user-attachments/assets/02afd90c-856c-4f38-8f94-6690422dc93b" />
