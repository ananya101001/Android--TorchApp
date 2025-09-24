# Android TorchApp 🔦

A minimal Android flashlight (torch) app built in **Java**. It toggles the device’s camera flash using `CameraManager` with a simple, responsive UI—great as a starter for sensor/control demos or coursework.

> Repo snapshot: Java-based Android project layout (`app/`, Gradle wrapper, etc.).  

---

## ✨ Features

- **One-tap flashlight toggle** (uses `CameraManager.setTorchMode`)
- **State-aware UI** (reflects ON/OFF status)
- **Lifecycle-safe** (releases resources appropriately)
- **Lightweight** (no ads, no extras)

---

## 🧱 Tech Stack

- **Language:** Java  
- **UI:** Android Views (or minimal Compose interop depending on template)  
- **API:** `CameraManager` (`android.hardware.camera2`)  
- **Build:** Gradle / Android Studio

---

## 📲 Requirements

- **Android Studio** Giraffe+ (or latest stable)
- **Android SDK** 21+ (Lollipop) recommended  
- A device with **camera flash** (physical device preferred)

---

## 🔐 Permissions

Add the following to `AndroidManifest.xml`:

```xml
<uses-permission android:name="android.permission.CAMERA" />
<uses-permission android:name="android.permission.FLASHLIGHT" />
```
## Run Locally

1. **Clone and open**
   ```bash
   git clone https://github.com/ananya101001/Android--TorchApp.git
   cd Android--TorchApp

flowchart TD
    B[User taps toggle] --> C[MainActivity handles click]
    C --> D[Camera manager setTorchMode cameraId onOff]
    D --> E{Call succeeds?}
    E -->|yes| F[Update UI state]
    E -->|no| G[Show error toast and log]

    
📂 Project Structure
Android--TorchApp/
├─ app/
│  └─ src/main/
│     ├─ java/.../MainActivity.java
│     ├─ res/layout/activity_main.xml
│     └─ AndroidManifest.xml
├─ gradle/wrapper/
├─ build.gradle
├─ settings.gradle
└─ gradle.properties


