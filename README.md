

---

# FPV Racing Drone 🚀

**High-Speed 180 km/h Drone | Designed, Built & Tuned by Swarnendu Bhattacharjee**

---

## 🧠 Overview

This project documents the complete development of a **First-Person View (FPV) racing drone** engineered for extreme performance, capable of reaching speeds over **180 km/h**.
It includes the **hardware architecture**, **PID-tuned firmware**, **build guide**, and **flight performance data** for advanced aerial control and stability.

---

## ⚙️ Key Features

* ⚡ **Max Speed:** ~189 km/h
* 🧩 **Modular Frame Design:** Lightweight custom made carbon-fiber structure
* 🧠 **Custom PID Tuning:** Precision control, response and acceleration maxing
* 📹 **FPV Setup:** Low-latency video feed for real-time control (5.2GHz)
* 🔋 **Optimized Power Delivery:** High-efficiency ESC & motor pairing
* 📈 **Flight Logs & Analysis:** Data visualization for tuning & diagnostics

---

## 🧩 Repository Structure

```
fpv-racing-drone/
│── hardware/        # Frame design, wiring schematics, motor/ESC details
│── firmware/        # Flight controller configuration files & tuning notes
│── docs/            # Design documentation, setup instructions, test logs
│── media/           # Flight videos, images, blackbox data
│── README.md
│── requirements.txt # (if control scripts/tools are used)
│── .gitignore
```

---

## 🛠️ Hardware Specifications

| Component             | Model / Specification             | Notes                            |
| --------------------- | --------------------------------- | -------------------------------- |
| **Frame**             | Custom-built (carbon fibre)       | Lightweight carbon fiber         |
| **Motors**            |        T-Motor F60 Pro IV 1750KV  | High torque and response         |
| **ESCs**              |        45A BLHeli_32              | Synchronized with FC             |
| **Flight Controller** |        iflight succex-e f405      | Configured via Betaflight        |
| **Propellers**        |        5-inch tri-blade           | Optimized for thrust and agility |
| **Battery**           |        6S 2300mAh LiPo 150C       | High discharge for burst speed   |
| **Camera**            |        Caddx / RunCam Phoenix 2   | FPV low-latency camera           |
| **VTX**               |        TBS Unify Pro HV           | Adjustable power output          |
| **Receiver**          |        Crossfire Nano RX          | Long-range communication         |
| **Antenna**           |        Pagoda RHCP                | Stable FPV signal                |

---

## 🧰 Software / Configuration

* **Firmware:** Betaflight 4.x
* **Configurator:** Betaflight / BLHeli Suite
* **Tuning:** PID and rate profiles optimized for racing conditions
* **Telemetry:** Optional data logging using Blackbox

---

## 🧱 Build Process

1. **Frame Assembly:** Mount arms, flight controller, and ESC stack.
2. **Wiring & Soldering:** Connect motors, power leads, VTX, and receiver.
3. **Firmware Setup:** Flash and configure Betaflight; calibrate sensors.
4. **PID Tuning:** Adjust roll, pitch, yaw parameters for stability.
5. **Flight Testing:** Perform hover and speed trials.
6. **Video Integration:** Configure FPV camera and VTX channel mapping.

---

## 🧪 Performance Testing

* **Top Speed Recorded:** 180 km/h (GPS verified)
* **Flight Time:** ~4 minutes (6S 1300mAh)
* **Hover Stability:** 9/10
* **Control Latency:** <20 ms
* **PID Tuning Logs:** Available in `/firmware/`

---

## 🎥 Media

All photos, videos, and flight recordings are stored in the [`/media`](./media) directory.
Include:

* Build process images
* FPV DVR footage
* Tuning test logs

---

## 🧩 Future Improvements

* Integration with GPS and telemetry OSD
* AI-based flight stabilization (using onboard MCU)
* FPV digital HD upgrade (e.g., DJI O3 Air Unit)
* Battery management monitoring script

---

## 🧑‍💻 Author

**Swarnendu Bhattacharjee**

* Founder, Builder, and Test Pilot
* GitHub: [@Swarnendu-Bhattacharjee](https://github.com/Swarnendu-Bhattacharjee)

---

## 📜 License

This project is released under the **MIT License**.
You are free to use, modify, and distribute this work with attribution.

---

✅ Copy-paste this **exact version** into your `README.md` file — all bold, emojis, and tables will render perfectly on GitHub.

Would you like me to also add a **tiny badge section** (Python version, license, repo size, etc.) at the top for a more professional look like major open-source projects?
