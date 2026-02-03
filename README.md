# Ultrasonic Distance Sensor (Arduino Uno R4 WiFi)

## Overview
Simple Arduino project that measures distance with an ultrasonic sensor (e.g., HC-SR04) and prints the result in centimeters to the Serial Monitor. Main source: `src/main.cpp`. Build configuration: `platformio.ini`.

## Hardware Required
\- Arduino Uno R4 WiFi  
\- Ultrasonic sensor (HC-SR04 or compatible)  
\- Jumper wires  
\- Breadboard (optional)

## Wiring
\- `VCC` \-\> 5V  
\- `GND` \-\> GND  
\- `Trig` \-\> digital pin `9` (matches `trigPin` in `src/main.cpp`)  
\- `Echo` \-\> digital pin `10` (matches `echoPin` in `src/main.cpp`)

## Software Requirements
\- PlatformIO (recommended) or Arduino IDE (Windows)  
\- `platformio.ini` configured for your board (the project includes `platformio.ini`)

## Build & Upload (PlatformIO)
1. Open a terminal in the project folder.  
2. Build: `platformio run`  
3. Upload: `platformio run --target upload`  
PlatformIO reads `platformio.ini` to select the board and upload settings.

## Build & Upload (Arduino IDE)
1. Open `src/main.cpp` in Arduino IDE.  
2. Select board: *Arduino Uno R4 WiFi* (Tools > Board).  
3. Select correct COM port (Tools > Port).  
4. Upload the sketch.

## Usage
1. Open the Serial Monitor at `9600` baud.  
2. The sketch prints the measured distance in centimeters once per second.

## Troubleshooting
\- No output: verify board selection and COM port.  
\- Incorrect readings: confirm wiring and that `Trig`/`Echo` pins match `src/main.cpp`.  
\- Unstable readings: ensure stable 5V supply and common ground between sensor and board.

## Files of interest
\- `src/main.cpp` — main sketch that triggers the sensor and prints distance.  
\- `platformio.ini` — PlatformIO configuration for building and uploading.

## License
MIT License. See repository `LICENSE` file for details.
