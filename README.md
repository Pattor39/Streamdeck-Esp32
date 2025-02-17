Welcome to the Streamdeck-Esp32 wiki!
# StreamDeck with ESP32-WROOM

## Overview
Our project, simply put, is a **Stream Deck**, with an **ESP32-WROOM** as the brain. Through an **Arduino-based code**, the device can connect to a computer via **Bluetooth**.

## Power Supply
The ESP32 needs to be powered either:
- Through the **computer connection** (USB)
- Directly from a **power source** (external supply)

## PCB Design
We designed a **custom PCB** for the ESP32, where:
- The **ESP32 pins** are connected to buttons.
- The buttons use a **pull-up configuration**.

## Functionality
The buttons execute commands made with Arduino, such as:
- 🔊 **Increasing and decreasing the volume**
- 🔇 **Muting**
- 🔄 **Refreshing the page**
- 🗑 **Clearing content**

This project allows for seamless **computer control via Bluetooth** with a simple, efficient hardware setup.
//
## ESP32 Board Installation in Arduino IDE

### Introduction
When working with ESP32 development boards in the Arduino IDE, users need to install the appropriate board definitions. This enables the IDE to compile and upload code specifically for ESP32 microcontrollers. The installation process requires adding a specific URL in the Arduino IDE's preferences.

### Why Add the URL: `https://dl.espressif.com/dl/package_esp32_index.json`

The URL `https://dl.espressif.com/dl/package_esp32_index.json` provides access to the ESP32 board definitions, tools, and libraries directly from Espressif's official servers. Adding this URL allows the Arduino IDE to download and install the necessary files for ESP32 development.

### Step-by-Step Explanation

1. **Open Arduino IDE:**
   Launch the Arduino IDE on your computer.

2. **Access Preferences:**
   Go to **File > Preferences** (or **Arduino > Preferences** on macOS).

3. **Add the URL:**
   In the "Additional Boards Manager URLs" field, paste the following URL:
   ```
   https://dl.espressif.com/dl/package_esp32_index.json
   ```

4. **Open the Boards Manager:**
   Go to **Tools > Board > Boards Manager**.

5. **Install ESP32:**
   Search for "ESP32" and click "Install" on the result provided by **Espressif Systems**.

### What Does the URL Do?

- **Downloads ESP32 Core:** Retrieves the necessary core files that extend Arduino IDE's compatibility to ESP32 boards.
- **Installs Required Tools:** Installs compilers, upload tools, and other dependencies.
- **Keeps Software Updated:** Ensures access to the latest updates and bug fixes from Espressif.

### Troubleshooting
If you encounter issues:
- Check your internet connection.
- Ensure the URL is correctly pasted.
- Restart the Arduino IDE and retry the installation.

### Conclusion
Adding the URL `https://dl.espressif.com/dl/package_esp32_index.json` is essential for enabling ESP32 development within the Arduino IDE. It provides the required software components directly from Espressif, ensuring a smooth and reliable development experience.

//

# ESP32 PCB Design and Schematic

## ESP32 PCB Design (First Image)
The **PCB design** follows a simple structure where:
- The **ESP32 pins** are connected to buttons.
- **Jumpers (JP4, JP5, JP6...)** allow enabling or disabling specific buttons.
- **Pull-up resistors** ensure proper button signal reading.

## Schematic Diagram (Second Image)
The schematic includes:
- **Pull-up resistors (R4, R5, R6, R7, R8, R9 - 10kΩ)** to keep GPIOs HIGH by default.
- **Jumpers (JP4 - JP9)** to enable or disable button inputs.
- **ESP32 connects via Bluetooth** to the computer.
- When buttons are pressed, the **Arduino code sends the corresponding command** to execute actions such as volume control, muting, refreshing, or clearing.

This setup ensures a stable and functional **Bluetooth-based Stream Deck** system. 🚀

//

## Installing `BLEKeyboard` Library in Arduino IDE

### Introduction

The `BLEKeyboard` library allows ESP32 microcontrollers to act as Bluetooth Low Energy (BLE) keyboards, sending keystrokes wirelessly to paired devices. This guide explains how to install and use the `BLEKeyboard` library in the Arduino IDE.

### Step-by-Step Installation Guide

1. **Open Arduino IDE:**
   Launch the Arduino IDE on your computer.

2. **Open Library Manager:**
   Go to **Tools > Manage Libraries**.

3. **Search for `BLEKeyboard`:**
   In the search bar, type `BLEKeyboard`.

4. **Install the Library:**
   Find the `BLEKeyboard` library by **T-vK** and click the **Install** button.

### Manual Installation (Alternative Method)

1. **Download the Library:**
   Go to the [[BLEKeyboard GitHub repository](https://github.com/T-vK/ESP32-BLE-Keyboard)](https://github.com/T-vK/ESP32-BLE-Keyboard) and download the repository as a ZIP file.

2. **Open Arduino IDE:**
   Launch the Arduino IDE.

3. **Install from ZIP:**
   Go to **Sketch > Include Library > Add .ZIP Library** and select the downloaded ZIP file.

