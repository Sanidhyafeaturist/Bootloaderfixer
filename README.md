# 🛠️ ESP8266 Bootloader Fixer

## Overview

This project implements a **bootloader fixer** for the NodeMCU (ESP8266) that allows for seamless recovery from firmware failures. If the current firmware is invalid, the device can load a backup firmware stored in the SPIFFS filesystem.

## Features

- 🌐 **Wi-Fi Connectivity**: Connects to your Wi-Fi network for remote management.
- 🔄 **Firmware Validity Check**: Verifies if the current firmware is valid before proceeding.
- 💾 **Backup Firmware Loading**: Loads a backup firmware from SPIFFS if the current firmware is invalid.
- 📡 **Over-the-Air (OTA) Updates**: Supports OTA firmware updates for easy deployment.

## Requirements

### Hardware

- NodeMCU (ESP8266) development board

### Software

- Arduino IDE with the ESP8266 board package installed
- Libraries: `ESP8266WiFi`, `FS`, `SPIFFS`, `ArduinoOTA`

## Setup Instructions

1. **Install Arduino IDE**:
   - Download and install the [Arduino IDE](https://www.arduino.cc/en/software).

2. **Install ESP8266 Board Package**:
   - Open the Arduino IDE.
   - Go to `File` > `Preferences`.
   - In the "Additional Board Manager URLs" field, add:
     ```
     http://arduino.esp8266.com/stable/package_esp8266com_index.json
     ```
   - Go to `Tools` > `Board` > `Board Manager`, search for "ESP8266", and install the package.

3. **Clone or Download the Repository**:
   - Clone this repository or download it as a ZIP file and extract it.

4. **Open the Code**:
   - Open the provided `.ino` file in the Arduino IDE.

5. **Configure Wi-Fi Credentials**:
   - In the code, replace `your_SSID` and `your_PASSWORD` with your actual Wi-Fi credentials.

6. **Upload the Code**:
   - Connect your NodeMCU to your computer.
   - Select the appropriate board and port in the Arduino IDE (`Tools` > `Board` > `NodeMCU 1.0 (ESP-12E Module)` and `Tools` > `Port`).
   - Click the upload button to upload the initial firmware.

7. **Upload Backup Firmware**:
   - Ensure you upload a valid firmware file named `backup.bin` to the SPIFFS filesystem using a separate sketch.

## Usage

- Open the Serial Monitor to observe the connection status to your Wi-Fi network.
- The device will check the firmware validity on startup and load the backup if necessary.
- Use the Arduino IDE for OTA updates by selecting "Upload" while connected to the same network.

## Important Notes

- 🗂️ Make sure the backup firmware is valid and thoroughly tested.
- 🔄 Modify the `isFirmwareValid()` function to fit your application's specific needs.
- ⚠️ Always have a backup plan when testing recovery mechanisms to avoid bricking your device.

## Future Enhancements

- 🚀 **Web Interface**: Develop a web interface for easier firmware management.
- 🔍 **Version Management**: Implement version checks to ensure compatibility of uploaded firmware.
- 🔒 **Enhanced Error Handling**: Add more robust error handling for increased reliability.

## License

This project is licensed under the MIT License. Feel free to modify and use the code for your own projects! 🎉
