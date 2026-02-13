# CanSAT Rocket Telemetry System — GPS Recovery Subsystem (Arduino, Multi-Sensor)

## Project Overview
This project implements a CanSAT/black box telemetry system for a category 2 rocket competition (2 km target altitude).  
The system streams and logs multi-sensor flight data, including altitude, engine thermals, acceleration, and GPS position, to enable safe post-landing recovery.  

**Role:** GPS subsystem development (NEO-M8N on Arduino UNO)  
**Technologies:** Arduino UNO, Adafruit Datalogger (SD card), NRF24L01 + PA + LNA, Thermocouple, MBE280, LSM6DS3, NEO-M8N GPS  

---

## System Architecture
![System Architecture](docs/SystemArchitecture.png) // this will link the path to the design

### Visual Diagram (Professional Image)
![System Architecture](docs/SystemArchitecture.png)

### Quick ASCII Diagram (Inline Reference)


**Data Flow:**  
// image perhaps of the data flow 

- GPS subsystem (your contribution) provides post-touchdown coordinates  
- SD card logs raw and structured sensor data  
- Wireless module streams real-time telemetry to ground station  

---

## Hardware Design
- **GPS:** NEO-M8N for accurate positioning  
- **Accelerometer/Gyroscope:** LSM6DS3  
- **Barometer:** MBE280 for altitude  
- **Thermocouple:** Engine thermal measurements  
- **Data Logging:** Adafruit Datalogger (SD card)  
- **Wireless Telemetry:** NRF24L01 + PA + LNA  

**Implementation Notes:**  
- Wiring diagram: `docs/WiringDiagram.png`  
- Rocket CAD: `docs/RocketCAD.png`  
- Antenna placement and power considerations included  

---

## Software Implementation
- Arduino code parses sensor data from all modules  
- GPS NMEA parsing and coordinate structuring  
- SD card logging (Adafruit Datalogger library)  
- Wireless telemetry transmission via NRF24L01  
- Modular code: separate files for GPS, thermocouple, barometer/accel  
- Example GPS snippet:

  // Snippet of my GPS code or what it may look like
