# Temperature node
PCB design for a temperature sensor based on SHT and ESP32.

#  Requirement Specifications

- Battery Operated: The node should operate on a battery with a lifespan of over a month.
- WiFi Connection: Supports 2.4 GHz WiFi to connect to a home network.
- MQTT Protocol: Publishes temperature and humidity data to an MQTT broker.
- Compact Design: Designed for easy placement in various locations around the home.
- Temperature and Humidity Reporting: Uses an SHT series sensor for accurate measurements.

# Functional Requirements Specification
## Electrical

- Battery Life: Should last more than a month on a single charge.
- Power Consumption: Optimized deep-sleep mode for low power consumption between readings.
- Input Voltage: 3.3V for ESP32 and 3V to 5V compatible for SHT sensors.
- Charging: Option for USB-C charging or solar panel for extended battery life.
- Voltage Regulation: Include a voltage regulator to ensure stable power delivery to ESP32 and the sensor.

## Mechanical

- Enclosure: IP65-rated enclosure for dust and water resistance if placed in areas prone to moisture.
- Size: Compact size, around 5cm x 5cm x 3cm, to fit easily on shelves or mounted on walls.
- Mounting (Optional): Option for wall mounting with screw holes or adhesive backing.
- Internal Antenna: PCB antenna for better WiFi range within the home.
- Access Ports: A small access port for USB charging and maintenance.

## Functional

- Data Reporting Interval: Configurable reporting interval (e.g., every 5 minutes, 10 minutes) to balance battery life and data frequency.
- Low Battery Alert: Sends an MQTT message when the battery level falls below a certain threshold.
- Temperature Range: Measures temperature from -20°C to +60°C.
- Humidity Range: Measures humidity from 0% to 100% relative humidity.
- OTA Updates: Supports Over-the-Air (OTA) firmware updates to improve functionality without physical access.
- Reconnection Logic: Automatically attempts to reconnect to WiFi and MQTT broker in case of network loss.
- Local Data Storage: Stores data temporarily in case of WiFi disconnection and uploads when the connection is restored.
