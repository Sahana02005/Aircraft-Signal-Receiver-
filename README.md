# Aircraft-Signal-Receiver-
A low-cost aircraft signal receiver project using RTL-SDR and Dump1090 to capture and decode ADS-B signals for real-time airplane tracking.
# Aircraft Signal Receiver Using RTL-SDR and Dump1090

## Overview
ADS-B (Automatic Dependent Surveillance–Broadcast) is used by commercial airplanes to broadcast their latitude, longitude, altitude, speed, and other flight information to air traffic controllers. These signals are transmitted at **1090 MHz** and can be received using an **RTL-SDR dongle**.  

In this project, we use the **Dump1090 program** on a Linux machine to decode ADS-B signals and create an **Aircraft Signal Receiver**. Apart from decoding, Dump1090 also hosts a **Google Maps web server** that displays the real-time locations of airplanes whose signals are being received.

---

## Features
- Real-time aircraft tracking
- Decodes ADS-B signals at 1090 MHz
- Displays aircraft position, altitude, and speed
- Web interface with Google Maps integration
- Works with low-cost RTL-SDR dongle

---

## Hardware Requirements
- RTL-SDR USB dongle
- Antenna tuned for 1090 MHz
- PC or Raspberry Pi

---

## Software Requirements
- Linux machine (Ubuntu/Debian recommended)
- Dump1090
- RTL-SDR drivers
- Python (optional, for visualization/logging)

---

##  Installation
1. Install RTL-SDR drivers:
   ```bash
   sudo apt-get install rtl-sdr

---

## Clone Dump1090
git clone https://github.com/antirez/dump1090
cd dump1090
make

## Run Dump1090:
./dump1090 --interactive --net

## To view aircraft positions on Google Maps.
Open your browser and go to:
http://localhost:8080

---

## Usage:
Run Dump1090 in interactive mode to see decoded aircraft data in the terminal.

Use the --net option to enable the web server for map visualization.

Example:
./dump1090 --interactive --net

---

## Sample Output
Hex    Flight   Altitude  Speed  Lat       Lon
ABC123 AI202    35000 ft  450 kt 12.9716   77.5946

