# OLED-Animation-on-ESP32-C3-with-0.96-OLED-Display
This project demonstrates how to display a smooth 24 FPS animation on a 0.96-inch OLED display  using the ESP32-C3 microcontroller. It uses the Adafruit GFX and SSD1306 libraries for easy graphics handling. The code includes frame data and animation logic to showcase advanced OLED animation techniques suitable for ESP32-based embedded projects.



# OLED Animation Advanced Example for ESP32-C3 with 0.96" OLED Display

This Arduino project displays a smooth 24 FPS animation on a 0.96-inch OLED display using an ESP32-C3 microcontroller.

---

## Hardware Requirements

- **Microcontroller:** ESP32-C3 (or compatible ESP32 series)
- **Display:** 0.96 inch OLED display, 128x64 pixels, SSD1306 driver (I2C interface)
- **Connections:**

| OLED Pin | ESP32-C3 Pin | Description         |
| -------- | ------------ | ------------------- |
| VCC      | 3.3V         | Power               |
| GND      | GND          | Ground              |
| SDA      | GPIO 8 (or any I2C SDA) | I2C Data      |
| SCL      | GPIO 9 (or any I2C SCL) | I2C Clock     |

> **Note:** Adjust SDA and SCL pins in code if you use different pins.

---

## Software Requirements

- Arduino IDE (version 1.8.13 or later recommended)
- ESP32 Board Support installed in Arduino IDE:
  - Open Arduino IDE > File > Preferences
  - Add this URL to **Additional Boards Manager URLs**:  
    `https://raw.githubusercontent.com/espressif/arduino-esp32/gh-pages/package_esp32_index.json`
  - Go to Tools > Board > Boards Manager, search for **esp32** and install.
- Libraries required:
  - Adafruit SSD1306  
  - Adafruit GFX

Install libraries via Arduino IDE Library Manager:

1. Go to Sketch > Include Library > Manage Libraries...
2. Search for and install **Adafruit SSD1306**
3. Search for and install **Adafruit GFX**

---

## How to Upload the Code

1. Clone or download this repository.
2. Open the `.ino` file in Arduino IDE.
3. Check and configure I2C pins if necessary in the code (`SDA` and `SCL`).
4. Select the board:
   - Go to Tools > Board > ESP32 Arduino > **ESP32C3 Dev Module**
5. Select the correct COM port under Tools > Port.
6. Click Upload.

---

## How to Use This Project

- Once uploaded, the ESP32-C3 will run the animation frames on the OLED display at ~24 FPS.
- Make sure your wiring matches the pins defined in the code.
- You can modify or add animation frames in `all_frames.h` file.

---

## Troubleshooting

- **OLED not displaying anything?**
  - Check wiring and power connections.
  - Verify I2C address (usually `0x3C` for 0.96" OLED).
  - Try scanning I2C bus with an I2C scanner sketch.
- **Compilation errors?**
  - Make sure all required libraries are installed.
  - Make sure ESP32 board support is installed.
- **Upload fails?**
  - Hold BOOT button on ESP32-C3 while uploading.
  - Check USB cable and drivers.











   
