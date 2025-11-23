🌐 IoT Comparative Demo – Azure IoT Hub


Project Overview
This project demonstrates a cloud IoT workflow using Azure IoT Hub as part of a comparative study between cloud and edge IoT platforms.
The workflow includes:

Simulated sensor (Python script) → Azure IoT Hub → Stream Analytics → Power BI Dashboard
Downlink control via Azure IoT Hub Direct Method.


🔍 What I Implemented

1. Azure IoT Hub Setup

Created an IoT Hub in Azure Portal.
Added an IoT device named virtualCapter.
Retrieved the device connection string for authentication.


2. Sensor Simulation (Python)

Developed a Python script in Google Colab:

Connected to Azure IoT Hub using the device connection string.
Sent random temperature and humidity values every 5 seconds. (10 messages)
Implemented Direct Method handler to allow downlink control (change telemetry interval).

3. Stream Analytics Job

Created a Stream Analytics job to process IoT Hub data:
  Input: IoT Hub messages.
  Output: Power BI dataset.
  Query: to collect data and take it from input to output
    
4. Power BI Dashboard

Connected Power BI to Stream Analytics output.
Built a real-time dashboard with:
 Temperature line chart.
 Humidity gauge.
 Card.

5. Downlink Control

Configured Direct Method in Azure IoT Hub:
 Method name: setFrequency.












