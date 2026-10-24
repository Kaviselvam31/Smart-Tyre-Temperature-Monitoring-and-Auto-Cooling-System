# Smart Tyre Temperature Monitoring and Auto-Cooling System

## Overview

The Smart Tyre Temperature Monitoring and Auto-Cooling System is an embedded systems project designed to monitor temperature using an LM35 temperature sensor and an ESP32 microcontroller. When the measured temperature exceeds a predefined threshold, the system activates a relay-controlled cooling mechanism and generates a warning through the Serial Monitor.

The project demonstrates temperature sensing, embedded C/C++ programming, relay control, and automated response logic.

## Objectives

- Monitor temperature in real time using an LM35 sensor.
- Process sensor readings using an ESP32 microcontroller.
- Generate a warning when the temperature exceeds a predefined threshold.
- Automatically activate and deactivate a cooling mechanism.
- Demonstrate hardware and software integration in an embedded system.

## Components Required

## Hardware Components Required

--->  Component Name andPurpose
ESP32 DevKit               – Controls the entire system and processes temperature sensor readings.
LM35 Temperature Sensor    – Measures the temperature and sends an analog signal to the ESP32.
Relay Module               – Switches the cooling fan ON and OFF based on the temperature threshold.
DC Cooling Fan             – Provides cooling when the temperature exceeds the predefined limit.
Breadboard                 – Helps assemble the circuit without soldering.
Jumper Wires               – Connect the ESP32, LM35 sensor, and relay module.
USB Cable and Power Supply – Supplies power to the ESP32 and enables programming.
External DC Power Supply   – Provides power to the cooling fan through the relay module.

## Working Principle

1. The LM35 senses temperature and generates an analog voltage.
2. The ESP32 reads the analog signal and estimates the temperature.
3. The measured temperature is compared with a predefined threshold.
4. If the temperature reaches 80°C, the relay activates the cooling fan.
5. When the temperature falls to 75°C or below, the cooling fan is switched off.
6. The temperature and system status are printed on the Serial Monitor.

The two temperature thresholds help prevent frequent switching when the temperature fluctuates around a single threshold.

## Software and Technologies

- Embedded programming: Arduino C++
- Microcontroller: ESP32
- Sensor interfacing: LM35
- Control mechanism: Relay module
- Development environment: Arduino IDE

## Project Structure

```text
smart-tyre-temperature-monitoring/
├── README.md
├── src/
│   └── smart_tyre_monitor.ino
├── circuit/
│   └── circuit_diagram.png
├── docs/
│   └── working_principle.md
├── images/
│   └── prototype.jpg
└── tests/
    └── test_results.md
```

## Testing

The prototype should be tested under controlled conditions:

- Check whether the sensor readings change with temperature.
- Verify that the high-temperature threshold activates the relay.
- Verify that cooling switches off after the temperature drops to the lower threshold.
- Compare sensor readings with a reference thermometer.
- Record the observed temperature, relay status, and test conditions.

Add actual measured results and prototype photographs after completing these tests.

## Future Enhancements

- Add an OLED display for local temperature monitoring.
- Integrate Wi-Fi-based remote monitoring using the ESP32.
- Add a buzzer for audible temperature alerts.
- Store temperature readings for trend analysis.
- Investigate suitable sensing methods for real tyre operating conditions.

## Safety Note

This repository demonstrates an educational prototype. The temperature thresholds and cooling mechanism have not been validated for real vehicle tyres. A road-going implementation would require appropriate sensor placement, environmental protection, reliable power, and automotive safety validation.

## Author

Developed as an academic project exploring embedded systems, temperature monitoring, and automated control.
