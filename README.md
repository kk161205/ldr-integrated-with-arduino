# LDR Sensor with Arduino Uno R4 WiFi

A minimal project that reads an LDR on analog pin `A0`, maps the 0\–1023 ADC value to 0\–100\% and prints both the raw value and percentage to the serial monitor at 9600 baud.

## Files
\- `src/main.cpp` \- Arduino sketch that reads the LDR and prints values.  
\- `platformio.ini` \- PlatformIO configuration (example / placeholder).

## Hardware
\- Board: Arduino Uno R4 WiFi  
\- Sensor: Light Dependent Resistor (LDR)  

## Software / PlatformIO
Example `platformio.ini` snippet (replace `board` with the exact PlatformIO board ID for your Uno R4 WiFi if different):
\```ini
[env:uno_r4_wifi]
platform = atmelsam
board = uno_r4_wifi
framework = arduino
monitor_speed = 9600
\```

Build and upload (from project root):
\-
\`pio run --target upload\`

Open serial monitor at 9600 baud:
\-
\`pio device monitor --baud 9600\`

If using CLion with PlatformIO integration, use the IDE run/upload and serial monitor UI.

## Behavior
\- Prints raw ADC value (0\–1023).  
\- Prints mapped light percentage (0\–100).  
\- Sampling delay is 300 ms (adjust in `src/main.cpp` as needed).

## Notes
\- Ensure the correct `board` value in `platformio.ini` for Arduino Uno R4 WiFi.  
\- If readings are unstable, try a different resistor value or add smoothing in software.
