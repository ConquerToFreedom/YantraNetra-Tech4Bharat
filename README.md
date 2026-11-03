# YantraNetra: Agentic Edge AI for MSME Predictive Maintenance

**Project Tracks:** Tech4Bharat (GAVS) & L&T TECHgium  
**Team Name:** Yantra Yodha

## The Problem

Small-scale manufacturing units run ageing machinery without condition monitoring. Unplanned breakdowns cost production days, emergency parts, and idle wages. Existing IoT solutions require expensive cloud connectivity and labelled fault data that MSMEs do not have.

## Our Solution

YantraNetra is a low-cost, offline-first retrofit. It uses on-device TinyML to learn a machine's normal behavior from vibration, current, and temperature. When an anomaly is detected, an autonomous agent diagnoses the cause and sends a Wi-Fi alert (via Telegram) to the owner's phone.

## System Architecture

* **Edge Controller:** STM32F446RE (Bare-metal C, TFLite Micro)
* **Sensors:** MPU6050 (Vibration), INA226 (Power), Hall Sensor (Speed), DS18B20 (Motor Temp), SHT31 (Ambient)
* **Agent Layer:** ESP8266 (NodeMCU) Wi-Fi Gateway

## Repository Structure

* `/firmware`: STM32 code, sensor drivers, and TinyML integration.
* `/ml`: Python training scripts for the unsupervised Autoencoder.
* `/agent`: ESP8266 Arduino code and Python scripts for the Telegram bot.
