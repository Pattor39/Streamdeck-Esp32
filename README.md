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

