# VOICE-CONTROL-BOT-USING-ARDUINO-AND-BLUETOOTH

This project implements a **voice-controlled robot** using **Arduino Uno**, an **HC-05 Bluetooth module**, and a **motor driver (L298N)**. The system receives voice commands via a smartphone app and executes basic robotic movements such as **forward, backward, left, right, and stop**.

---

## 🔧 Hardware Components

| Component           | Quantity | Description                              |
|---------------------|----------|------------------------------------------|
| Arduino Uno         | 1        | Microcontroller board                    |
| HC-05 Bluetooth Module | 1     | For wireless voice command communication |
| L298N Motor Driver  | 1        | Controls motor directions and speed      |
| DC Motors (BO)      | 4        | Front wheels (2) and Back wheels (2)     |
| Robot Chassis       | 1        | Base structure                           |
| Smartphone (Android)| 1        | With voice control app (e.g., Arduino Bluetooth Control) |
| Power Source        | 1        | used 2000mAh or Battery (9V or 12V your convinent) |
| Jumper Wires        | –        | For connections                         |

---

## 🧠 Working Principle

1. **Voice Command Input**:  
   User speaks into a mobile app (like “Bluetooth Voice Control”).
   
2. **Bluetooth Transmission**:  
   The app sends a corresponding character over Bluetooth.

3. **Arduino Processing**:  
   Arduino receives this character and matches it to a motor control command.

4. **Motion Execution**:  
   The L298N motor driver activates the motors accordingly.

---

## 📂 Project Structure

| File                  | Description                          |
|------------------------|--------------------------------------|
| `VOC_bluetooth.ino`        | Arduino sketch controlling motor logic |
| `README.md`            | Project documentation               |
| `Voice Controlled Robot - Circuit diagram.png`  | Wiring and connection diagram |

---

## 📝 Arduino Code Summary

The Arduino sketch listens for characters sent via Bluetooth and controls the motors:

| Voice Command | Bluetooth Char | Action         |
|---------------|----------------|----------------|
| "Forward"     | `F`            | Moves forward  |
| "Backward"    | `B`            | Moves backward |
| "Left"        | `L`            | Turns left     |
| "Right"       | `R`            | Turns right    |
| "Stop"        | `S`            | Stops the bot  |

Each command triggers digital signals to the **L298N module**, setting motor direction.

---

## 🔌 Circuit Diagram

> ![Voice Controlled Robot - Circuit diagram](https://github.com/user-attachments/assets/ecaa2d8e-1367-4015-a19f-7f45df50d67b)

> Includes connections:
- HC-05 TX → Arduino RX  
- HC-05 RX → Arduino TX (with voltage divider)  
- Motor driver IN1/IN2/IN3/IN4 → Arduino digital pins  
- VCC, GND, and motor terminals

---

## 📲 Smartphone App Setup

- Install: **Arduino Bluetooth Control"** from Play Store
- https://play.google.com/store/apps/details?id=com.broxcode.arduinobluetoothfree&pcampaignid=web_share
- Pair with **HC-05 (Default password: 1234 or 0000)**
- Start speaking commands like: `"forward"`, `"stop"`, etc.

---

## ✅ Demo Output

![Voice Control Bot](https://github.com/user-attachments/assets/34deee64-dc81-4a28-879a-61094ea07125)


---

## 🚀 Future Enhancements

- Add obstacle avoidance with ultrasonic sensor
- Control via IoT (Wi-Fi/Cloud-based interface)
- Voice recognition using offline modules (like Elechouse VR3)
- Integrate speed control using PWM

---

## 👩‍💻 Author

- **Harshitha A**  
 Developed by HARSHITHA ARUNACHALA Undergraduate Student, B.E. Electronics and Communication Engineering (ECE)
  GitHub: [@HARSHITHA292003](https://github.com/HARSHITHA292003)

---

