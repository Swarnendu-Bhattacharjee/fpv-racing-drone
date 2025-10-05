---

# 🧠 Firmware Documentation – FPV Racing Drone

## ⚙️ Overview

This folder contains all configuration, tuning, and firmware-related files for the **FPV Racing Drone** project.
It includes **Betaflight**, **BLHeli_32**, and **receiver mapping** details, as well as PID tuning logs and telemetry setup information.

---

## 🪪 Firmware Details

| Parameter             | Specification                     |
| --------------------- | --------------------------------- |
| **Flight Controller** | Betaflight F7 / F4                |
| **Firmware Version**  | Betaflight 4.x                    |
| **Configurator**      | Betaflight Configurator (Desktop) |
| **ESC Firmware**      | BLHeli_32 (v32.x)                 |
| **Receiver Protocol** | CRSF / SBUS                       |
| **Telemetry**         | SmartPort / Crossfire             |
| **Radio Used**        | Radiomaster TX16S / Tango 2       |

---

## 🎛️ PID Profiles

| Profile       | Roll (P/I/D) | Pitch (P/I/D) | Yaw (P/I/D) | Description                            |
| ------------- | ------------ | ------------- | ----------- | -------------------------------------- |
| **Profile 1** | 45 / 50 / 30 | 50 / 55 / 35  | 60 / 60 / 0 | Default tune (initial test)            |
| **Profile 2** | 42 / 48 / 28 | 47 / 53 / 33  | 58 / 58 / 0 | Reduced overshoot for smoother control |
| **Profile 3** | 40 / 45 / 25 | 45 / 50 / 30  | 56 / 56 / 0 | Final optimized tune for racing        |
| **Profile 4** | —            | —             | —           | Reserved for high-speed testing        |

### Notes

* Tested under calm wind conditions (~4 m/s).
* Yaw D-term disabled for noise reduction.
* Verified using Betaflight Blackbox Analyzer.

---

## ⚡ ESC Configuration (BLHeli_32)

### ESC Details

| Parameter                  | Value                            |
| -------------------------- | -------------------------------- |
| **Brand / Model**          | Holybro Tekko32 F3 45A (example) |
| **Firmware**               | BLHeli_32 (v32.8)                |
| **PWM Frequency**          | 48 kHz                           |
| **Startup Power**          | 0.75                             |
| **Beacon Delay**           | 10 min                           |
| **Brake on Stop**          | Enabled                          |
| **Demag Compensation**     | High                             |
| **Motor Timing**           | 22°                              |
| **Temperature Protection** | 140 °C                           |

**Motor Direction:** Normal
**ESC Protocol:** DShot600

---

## 🛰️ Receiver & Channel Mapping

| Channel | Function    | Input Type | Notes                 |
| ------- | ----------- | ---------- | --------------------- |
| 1       | Roll        | A          | Mode 1                |
| 2       | Pitch       | E          | Mode 1                |
| 3       | Throttle    | T          | Calibrated            |
| 4       | Yaw         | R          | —                     |
| 5       | Arm         | Switch A   | Primary arming switch |
| 6       | Flight Mode | Switch B   | Angle / Horizon       |
| 7       | Buzzer      | Switch C   | Optional              |
| 8       | Turtle Mode | Switch D   | Flip-over enabled     |

**Receiver Protocol:** CRSF (TBS Crossfire Nano RX)
**Failsafe:** Drop throttle + hold last roll/pitch for 1 s then disarm
**RSSI Channel:** 8

---

## 📡 Telemetry Setup

### Hardware

* **Flight Controller:** Betaflight F7
* **Receiver:** Crossfire Nano RX
* **Protocol:** CRSF
* **Telemetry Link:** SmartPort

### Configuration Steps

1. Enable telemetry in Betaflight CLI:

   ```
   feature TELEMETRY
   save
   ```
2. Connect TX pad (UART2) → RX on receiver.
3. Verify telemetry in the transmitter (TX16S / Tango 2).
4. Add telemetry sensors for:

   * Battery Voltage
   * RSSI
   * GPS (if enabled)
   * Current Draw
   * Flight Mode Indicator

### Notes

* Default telemetry update rate: **1 Hz** (can be increased to **5 Hz**).
* On-Screen Display (OSD) overlay enabled via Betaflight.

---

## 🧾 File Descriptions

| File                         | Description                                                |
| ---------------------------- | ---------------------------------------------------------- |
| `betaflight_config_dump.txt` | Raw Betaflight CLI configuration dump (`diff all` output). |
| `esc_settings.txt`           | BLHeli_32 configuration parameters.                        |
| `pid_profiles.md`            | PID tuning profiles and notes.                             |
| `receiver_mapping.md`        | Channel map and input switch configuration.                |
| `telemetry_setup.md`         | Telemetry connection and setup guide.                      |

---

## 🔧 Notes & Maintenance

* Always back up your Betaflight configuration before flashing.
* Recalibrate accelerometer and radio after every firmware update.
* Check motor direction after each re-flash.
* Update ESC firmware periodically for stability improvements.

---

## 🧑‍💻 Author

**Swarnendu Bhattacharjee**
FPV Drone Developer & Builder
GitHub: [@Swarnendu-Bhattacharjee](https://github.com/Swarnendu-Bhattacharjee)

---

✅ **To add:**

* Betaflight CLI dump (`diff all`) → `betaflight_config_dump.txt`
* BLHeli settings export → `esc_settings.txt`

---

### 📤 Commit Commands

```bash
cd /home/swarnendu/fpv-racing-drone
git add firmware/README.md
git commit -m "Added firmware documentation README for FPV Drone"
git push
```

---
