---



\# 📡 Telemetry Setup



\## Hardware

\- \*\*Flight Controller:\*\* Betaflight F7

\- \*\*Receiver:\*\* Crossfire Nano RX

\- \*\*Protocol:\*\* CRSF

\- \*\*Telemetry Link:\*\* SmartPort



\## Configuration Steps

1\. Enable telemetry feature in Betaflight CLI:

feature TELEMETRY

save

2\. Connect TX pad (UART2) → RX on receiver.

3\. Verify telemetry data in radio (TX16S / Tango 2).

4\. Configure telemetry sensors:

\- Battery voltage

\- RSSI

\- GPS (if enabled)

\- Current draw

\- Flight mode indicator



\## Notes

\- Telemetry update rate: 1Hz (can be increased to 5Hz for smoother OSD updates)

\- OSD telemetry overlay configured in Betaflight.



---

