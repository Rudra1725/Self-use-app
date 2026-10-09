# 📍 Reached — Automated Campus Arrival & Safety Check-in

[![Platform](https://img.shields.io/badge/Platform-Android-green.svg)](https://developer.android.com/)
[![Language](https://img.shields.io/badge/Language-Java-orange.svg)](https://www.java.com/)
[![License](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)

**Reached** is a lightweight, background-driven Android utility designed to automate daily transit safety check-ins. Using hardware-efficient geofencing, it silently detects when you cross your college campus boundary and automatically dispatches an arrival confirmation to your parents—eliminating the need for manual check-ins after daily bike commutes.

---

## ✨ Features

- 🛰️ **Geofencing API Integration**: Leverages Google Play Services Geofencing to monitor campus perimeter entry with minimal battery impact.
- ⏰ **Daily Auto-Arm Schedule**: Uses Android `WorkManager` to automatically arm tracking before morning commute hours and disarm after arrival.
- 🎯 **Interactive Map Picker**: Easily set and customize target destination coordinates and geofence radius.
- 📡 **Radar Status UI**: Clean, centered radar animation interface displaying active monitoring states and geofence status in real-time.
- ✉️ **Zero-Friction Notification**: Automatically triggers arrival confirmation upon boundary crossing.

---

## 🛠️ Architecture & Tech Stack

- **Language**: Java
- **Location Services**: [Google Play Services Location & Geofencing API](https://developers.google.com/android/reference/com/google/android/gms/location/GeofencingClient)
- **Background Tasks**: [Android Jetpack WorkManager](https://developer.android.com/topic/libraries/architecture/workmanager)
- **Maps**: Google Maps SDK for Android
- **UI Components**: Material Components & Custom Radar Pulse Animation View

---

## 📂 Project Structure

```text
app/src/main/
├── java/com/.../reached/
│   ├── ui/               # Activities, radar visualizer, and map picker
│   ├── geofence/         # GeofenceBroadcastReceiver, GeofenceHelper
│   ├── workers/          # AutoArmWorker (WorkManager background tasks)
│   └── utils/            # Permissions, notification handlers, preferences
└── res/
    ├── layout/           # Activity & radar UI layouts
    └── values/           # Colors, styles, strings
