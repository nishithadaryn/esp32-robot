
```markdown
# 🤖 ESP32 Robot Controlled by PS4 Controller

This project demonstrates how to control an **ESP32-based robot** using a **PS4 controller** via Bluetooth. The robot receives commands wirelessly and moves accordingly.

## 🧰 Requirements

### 🛠️ Hardware

- ESP32 development board
- PS4 Controller (DualShock 4)
- Robot platform (motors/servos/wheels)
- Motor driver (e.g., L298N or similar)
- Battery pack
- Jumper wires and breadboard

### 💻 Software

- [Arduino IDE](https://www.arduino.cc/en/software)
- [PS4 Bluetooth Library for ESP32](https://github.com/aed3/PS4-esp32) *(or similar)*
- USB Driver: [CP210x Drivers](https://www.silabs.com/developers/usb-to-uart-bridge-vcp-drivers)


## ⚙️ Setup Instructions

### 1. Install Arduino Support for ESP32

- In Arduino IDE, go to:
  - **File > Preferences** → Add this URL to "Additional Board URLs":

    https://raw.githubusercontent.com/espressif/arduino-esp32/gh-pages/package_esp32_index.json

  - Then go to **Tools > Board > Boards Manager** and install "esp32".


### 2. Install Required Libraries

In **Arduino IDE**, install:

- `PS4-esp32` library  
- `Servo.h` (for servo motor control)

> Go to **Sketch > Include Library > Manage Libraries**

---

### 3. Pair PS4 Controller

Upload the code from `PS4Controller` folder to ESP32.  
Open **Serial Monitor**, you'll see the MAC address.

#### On PS4 Controller:
- Hold **Share + PS** button until the LED flashes.
- Wait for ESP32 to pair and log `Controller Connected!` message.

---

### 4. Upload the Robot Code

Use the sketch in `ESP32Servo/` or `code/` to move motors/servos based on joystick or button input.

---

## 🎮 Controls (Sample Mapping)

| PS4 Input       | Action           |
|----------------|------------------|
| Left Stick     | Move forward/backward/turn |
| Button X       | Stop             |
| R1/L1          | Speed control    |
| Triangle/Circle| Custom actions   |

> Customize mappings in `loop()` based on your robot design.


## 🖥️ Driver Installation (Windows)

Use the `CP210x_Windows_Drivers/` if your ESP32 board is not detected over USB.





