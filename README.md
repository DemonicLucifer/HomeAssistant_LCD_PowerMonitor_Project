ESP32 Home Assistant Power Monitor


Overview

This project fetches real-time power consumption and monthly usage from Home Assistant via its REST API. It calculates electricity cost and displays it on a 16x2 I2C LCD. When power usage drops below a threshold or data stops updating (indicating power outage), it switches to a UPS power warning mode, showing remaining UPS runtime and battery charge with no annoying screen flicker.

Features

Connects to WiFi and Home Assistant securely with a bearer token

Fetches current power consumption and monthly kWh usage

Calculates and displays cost based on configurable rate

Detects power outage by monitoring stale sensor data

Displays UPS runtime and battery charge during outages

Clean, flicker-free LCD display updates

Requirements

ESP32 board

16x2 I2C LCD (address 0x27)

Home Assistant with REST API access

Power consumption sensor in Home Assistant

UPS runtime and battery charge sensors in Home Assistant

Setup

Configure your WiFi credentials in the code.

Set your Home Assistant IP, port, and long-lived access token.

Update sensor entity IDs to match your setup.

Adjust electricity cost per kWh as needed.

Upload to your ESP32 and enjoy real-time monitoring.

Notes

The code assumes power consumption data updates regularly - if no update for 5 seconds, it assumes power outage.

The UPS runtime sensor value is expected in seconds and is converted to minutes for display.

No $/£ sign by default, but can be added easily.

License
MIT License - Feel free to use, modify, and share.

