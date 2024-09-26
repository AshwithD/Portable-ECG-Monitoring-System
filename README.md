 Portable ECG Monitoring System

This repository contains the code and documentation for a  "Portable ECG Monitoring System" using an ATmega328P microcontroller, AD8232 ECG sensor, and a 128x64 OLED display.
The system measures the user's ECG (electrocardiogram) data and displays a real-time graph along with the ECG value on an OLED screen.

Features:
- Real-time ECG monitoring.
- Displays ECG value and graph on a 128x64 OLED display.
- Uses an AD8232 sensor module to detect heart electrical activity.
- Low-power consumption with a compact design for portability.

Hardware Components
- ATmega328P Microcontroller
- AD8232 ECG Sensor Module
- 128x64 OLED Display (I2C)
- Power Supply: 9V Battery 
- Capacitors: 10µF, 22pF, 0.1µF, 0.33µF
- Resistors: 1kΩ,10k
- Breadboard and Jumper Wires

Software Requirements
- Arduino IDE for writing and uploading the code.
- U8glib Library for controlling the 128x64 OLED display.

 Installation
1. Clone this repository:
git clone https://github.com/AshwithD/Portable-ECG-Monitoring-System.git

2. Install necessary libraries:
- Open Arduino IDE.
- Go to Sketch > Include Library > Manage Libraries.
- Search for `U8glib` and install it.

3. Upload the Code:
- Open the `ecg_oled_display.ino` file in Arduino IDE.
- Select the correct board and port:
  - Board: `ATmega328P`
  - Programmer: `Arduino Uno` 
- Upload the code to the microcontroller.

 Usage:
1. Power on the system using the power supply .
2. The OLED display will start showing the ECG value and a real-time graph of the heart activity.
3. Connect the ECG sensor pads to the user to begin recording.

 How It Works:
The AD8232 ECG sensor module detects the heart’s electrical activity and outputs an analog signal proportional to the heart rate. 
This signal is read by the ATmega328P via an analog pin, processed, and then displayed as both an ECG value and a moving graph on the OLED display.
The system refreshes the graph every cycle to simulate continuous monitoring.

Code Overview

- `setup()`: Initializes the OLED display and serial communication for debugging.
- `loop()`: Reads the ECG value from the AD8232 sensor and updates the OLED display with the ECG value and waveform graph.
- `drawECGGraph()`: Handles the rendering of the ECG graph and value on the OLED screen.

 Future Improvements:
- Add heart rate calculation based on ECG signal.
- Use a higher resolution display or TFT for better graph clarity.
- Add Bluetooth functionality to transmit ECG data to a mobile app.

License:
This project is licensed under the MIT License - see the LICENSE file for details.

Acknowledgments
- AD8232 Sensor Module documentation and reference designs.
- U8glib Library for handling OLED displays.


Let me know if you’d like to add anything or make changes!
