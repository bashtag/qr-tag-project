# QR Tag Project

### Team: CUBUK  
### Date: 30.05.2024  
### University: Gebze Technical University  

---

## Table of Contents:
- [Introduction](#introduction)
- [Project Structure](#project-structure)
- [Installation Guide](#installation-guide)
- [Module Descriptions](#module-descriptions)
  - [Location Tracking Module -Arduino/ESP32-](#location-tracking-module)
  - [Game Server and 3D Modelling Module -Unreal Engine-](#game-server-and-3d-modelling-module)
  - [Game Logic Module](#game-logic-module)
  - [Mobile Application Module -Android-](#mobile-application-module)
  - [Desktop Application -Qt-](#desktop-application)
- [Challenges Faced](#challenges-faced)
- [Conclusion](#conclusion)
- [Additional Files](#additional-files)
- [Collaborators](#collaborators)
---

## Introduction
The **QR Tag Project** is an interactive gaming experience combining mobile QR code scanning, location tracking, and real-time game mechanics. Players engage in a competitive game where they tag each other by scanning QR codes. The project consists of multiple modules, including location tracking with ESP32 devices, a mobile application for interaction, a game server for real-time updates, and a 3D game area modeled in Unreal Engine 5.

---

## **Watch the Gameplay and Implementation Video**
[![Watch the Video](https://img.youtube.com/vi/42vSmNZDn74/0.jpg)](https://youtu.be/42vSmNZDn74?si=aFr2VjpI9jUzaMdx)

---

## **Visit Our Website**
[Visit the Website](https://ardaardac.wixsite.com/my-site-3)

---

## Project Structure
qr-tag-project/\
├── AndroidApp/\
├── Arduino/\
├── UnrealEngine/\
├── QtApp/\
└── README.md

Each folder contains source codes and necessary files for specific modules.

## Installation Guide
Follow the instructions below to install and run the components of the QR Tag Project:

### Server and Desktop App (Qt)
1. Install Qt and required tools:\
sudo apt update sudo apt install qt5-default qtcreator build-essential

2. Generate the Makefile:\
qmake server_desktop_app.pro make

3. Run the server application:\
./server_desktop_app


### Mobile Application (Android)
1. Install Android Studio and open the project:
- Go to `AndroidApp/` directory.
- Select "Open Existing Android Project" in Android Studio.
2. Sync Gradle:
- Click "Sync Project with Gradle Files" button.
3. Build the APK:
- Go to Build > Build APK(s).
4. Run on a connected Android device.

### ESP32 Codes (Arduino)
1. Install the Arduino CLI:\
curl -fsSL https://raw.githubusercontent.com/arduino/arduino-cli/master/install.sh | sh sudo mv bin/arduino-cli /usr/local/bin/

2. Set up ESP32 board:\
arduino-cli config init arduino-cli config set board_manager.additional_urls https://raw.githubusercontent.com/espressif/arduino-esp32/gh-pages/package_esp32_index.json arduino-cli core install esp32

3. Compile ESP32 code:\
arduino-cli compile --fqbn esp32:esp32\
scanner.ino


---

## Module Descriptions

### 📍Location Tracking Module
**Purpose**: Track player positions using ESP32 devices in the game area.  
**Technologies**: ESP32, C/C++.  
**Development Environment**: Arduino IDE.  
**Challenges**: Signal strength issues and frequent disconnections due to large game area.  

### 🎮Game Server and 3D Modelling Module
**Purpose**: Manage game settings, track player positions, and visualize the game area.  
**Technologies**: Unreal Engine 5, C++, TCP/UDP Protocols.  
**Development Environment**: Visual Studio, Unreal Engine 5.  
**Challenges**: Issues with real-time data integration and 3D model collisions.

### 🧩Game Logic Module
**Purpose**: Implement game rules and mechanics (health points, tagging, score management).  
**Technologies**: C/C++, Arduino.  
**Challenges**: Delays in physical indicators (LEDs), ensuring accurate game rule enforcement.

### 📱Mobile Application Module
**Purpose**: Provide an interface for players to interact with the game, display real-time stats, and scan QR codes.  
**Technologies**: Android NDK, ZXing Library.  
**Development Environment**: Android Studio.  
**Challenges**: QR scanning issues with certain devices and preventing exploitative gameplay mechanics.

### 💻Desktop Application
**Purpose**: Manage the server-side logic, display 3D visualization of the game area, and handle game-related events.  
**Technologies**: Qt, C++.  
**Challenges**: Configuring the 3D model and managing server IP configurations.

---

## Challenges Faced
1. **Location Tracking**: Difficulty in obtaining real-time location updates due to ESP32 signal limitations.
2. **Game Server**: Problems with player movement and real-time data synchronization in the 3D model.
3. **Mobile App**: Camera issues with QR scanning and preventing misuse of game mechanics (e.g., self-kill).
4. **Game Logic**: Managing game rules with physical indicators like LEDs using multi-threading.

---

## Conclusion
The QR Tag project successfully combines mobile technology, server communication, and real-time game mechanics to offer an engaging multiplayer experience. Despite several technical challenges, each module was developed and tested thoroughly to create a cohesive gaming system.

## Additional Files
For more information, including a demonstration video, our website, the final project report and user manual, you can access the following links:
- [Gameplay and Implementation Video](https://youtu.be/42vSmNZDn74?si=aFr2VjpI9jUzaMdx)  
- [Project Website](https://ardaardac.wixsite.com/my-site-3)  
- [Project Files (Final Report and User Manual)](https://drive.google.com/drive/folders/17KQuRK2ZjIPfvACE4FMA6-GAQMbPVH46?usp=sharing)  

## 🤝Collaborators
[@bashtag](https://github.com/bashtag):
- Led the 3D reconstruction component development using Unreal Engine C++.  
- Implemented Native C++ components for Android and designed UI using Kotlin and XML.
- Established  socket communication between components.
- Contributed and debugged the Qt server app and the ESP module.

[@ardac67](https://github.com/ardac67):
- Led the development of the Qt Server module
- Led the ESP module
- Established socket communication between components.
- Procured necessary hardware components

[@aliasimcoskun](https://github.com/aliasimcoskun): 
- Originated the QR Tag idea (limited to QR Tag functionality; 3D and other location-related features were conceptualized by Prof. Dr. Erkan Zergeroğlu).
- Redesigned the front-end of the mobile application using Kotlin (limited to XML files for the UI).
- Edited project video.
- Authored all required project reports.
- Creating simple website for demo.

@alperenduran:
- Designed the breadboard for the ESP module.
