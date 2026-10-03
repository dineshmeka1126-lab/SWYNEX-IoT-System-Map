# SWYNEX IoT System Map

## Task 1: IoT System Map

### Project Title

**Smart Room Temperature Monitoring System**

## 1. Introduction

The Smart Room Temperature Monitoring System is a simple IoT system designed to monitor room temperature and humidity continuously.

The sensor collects environmental data and sends it through a wireless connection to a cloud platform. The collected information can then be displayed on a dashboard so that users can monitor room conditions remotely.

## 2. IoT System Components

### A. Sensor Layer

**Temperature and Humidity Sensor – DHT11/DHT22**

The sensor measures:

* Room temperature
* Humidity

### B. Connectivity Layer

The sensor data is transmitted using **Wi-Fi**.

Wi-Fi allows the IoT device to connect to the Internet and send sensor readings to the cloud.

### C. IoT Processing Device

An **ESP32** can collect the sensor readings and send the data to the cloud.

Main functions:

1. Read sensor data
2. Process the readings
3. Connect to Wi-Fi
4. Send data to the cloud

### D. Cloud Layer

The cloud platform receives and stores the sensor data.

Possible platforms include:

* ThingSpeak
* Firebase
* AWS IoT
* Microsoft Azure IoT

The cloud provides data storage, processing and remote access.

### E. Dashboard Layer

The dashboard displays:

* Current temperature
* Current humidity
* Temperature graph
* Humidity graph
* Historical readings
* Alert status

## 3. IoT System Architecture

```text
+----------------------------+
|      ROOM ENVIRONMENT      |
| Temperature + Humidity     |
+-------------+--------------+
              |
              v
+----------------------------+
|       DHT11 / DHT22        |
|          SENSOR            |
+-------------+--------------+
              |
              | Sensor Data
              v
+----------------------------+
|           ESP32            |
|     IoT Processing Unit    |
+-------------+--------------+
              |
              | Wi-Fi
              v
+----------------------------+
|         INTERNET           |
+-------------+--------------+
              |
              v
+----------------------------+
|       CLOUD PLATFORM       |
|   Data Storage & Processing|
+-------------+--------------+
              |
              v
+----------------------------+
|        WEB DASHBOARD       |
| Temperature: 28°C          |
| Humidity: 65%              |
| Temperature Graph          |
| Humidity Graph             |
+-------------+--------------+
              |
              v
+----------------------------+
|            USER            |
|      Mobile / Laptop       |
+----------------------------+
```

## 4. Data Flow

```text
Room Environment
       ↓
Temperature & Humidity Sensor
       ↓
ESP32
       ↓
Wi-Fi
       ↓
Internet
       ↓
Cloud Platform
       ↓
Database
       ↓
Dashboard
       ↓
User
```

### Data Flow Explanation

1. The sensor measures room temperature and humidity.
2. The sensor sends the readings to the ESP32.
3. The ESP32 processes the readings.
4. The ESP32 sends the data through Wi-Fi.
5. The data reaches the cloud platform.
6. The cloud stores the collected data.
7. The dashboard retrieves the data.
8. The user can monitor the readings remotely.

## 5. Example Sensor Data

| Time     | Temperature | Humidity |
| -------- | ----------: | -------: |
| 10:00 AM |        27°C |      62% |
| 11:00 AM |        28°C |      64% |
| 12:00 PM |        29°C |      66% |
| 01:00 PM |        30°C |      68% |
| 02:00 PM |        29°C |      67% |

## 6. Alerts

The system can generate an alert when the temperature exceeds a predefined limit.

```text
Temperature > 35°C
        ↓
High Temperature Detected
        ↓
Send Alert to User
```

## 7. Benefits

* Real-time monitoring
* Remote monitoring
* Temperature and humidity measurement
* Cloud data storage
* Historical data analysis
* Dashboard visualization
* Automatic alerts

## 8. Applications

This system can be used in:

* Homes
* Classrooms
* Offices
* Laboratories
* Server rooms
* Warehouses
* Greenhouses

## 9. Conclusion

The Smart Room Temperature Monitoring System demonstrates the basic architecture of an IoT system.

It connects sensors, an IoT processing device, Wi-Fi connectivity, cloud storage and a dashboard into a complete data flow.

The main IoT process is:

**SENSE → CONNECT → CLOUD → ANALYZE → DISPLAY → USER**

This conceptual system can later be expanded with additional sensors, automatic controls, notifications and data analytics.
# SWYNEX-IoT-System-Map
IoT System Map for a Smart Room Temperature Monitoring System, documenting sensors, connectivity, cloud data flow, dashboard, and remote monitoring.
