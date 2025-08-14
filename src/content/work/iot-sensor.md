---
title: IoT Sensors Dashboard
publishDate: 2025-08-10 00:00:00
status: done
img: /assets/works/iot_sensor.png
img_alt: IoT sensors dashboard
description: |
  A full-stack project for collecting and visualizing sensors data.
  The focus was on working with ESP32-based devices, optimizing battery usage, and building a modern dashboard to monitor various measurements.
link: ''
tags:
  - NestJS
  - ReactJS
technos:
  - ApexCharts
  - TanStack Router
  - TanStack Query
  - TanStack Form
  - DaisyUI
  - Tailwind CSS
  - I18next
  - Zod
  - Coolify
  - GitHub Actions
---

## From hardware to dashboard

> I wanted to explore the full journey of an IoT project: from sensor data acquisition to visualization in the browser.

This project was my first deep dive into IoT, working with **ESP32** boards and various sensors (temperature, humidity, light, etc.).  
On the hardware side, I learned how to manage low-power modes to extend battery life and send data periodically via Wi-Fi.  
On the software side, I built a responsive dashboard to display this data in an attractive, interactive way.

While my background was more web focused, I used this opportunity to connect hardware, APIs, and UI in one coherent system.

### Why this project?

I wanted something practical and visually engaging for my portfolio, but also technical enough to explore:
- Low-level constraints (battery, connectivity)
- Back-end API design for IoT data
- Modern front-end state management and routing
- Real-time and historical data visualization

### Key aspects

- <span class="title">Device communication</span>: ESP32 devices send periodic measurements to the backend API.
- <span class="title">Battery optimization</span>: Sleep cycles and optimized Wi-Fi usage to extend autonomy.
- <span class="title">Data storage & access</span>: Server-side logic to store and retrieve time-series data efficiently.
- <span class="title">Dashboard UI/UX</span>: Multiple chart types for different measurements (line charts, battery gauges, column charts for light levels, etc.).

### Features

- Real-time and historical charts for temperature, humidity, light levels, etc.
- Battery level indicators for each device.
- Fully responsive dashboard UI built with Tailwind + DaisyUI.

### Libraries / technologies used

- **Frontend**: React 19, TanStack Router/Query/Form, ApexCharts, Tailwind CSS, DaisyUI, i18next, Zod
- **Backend**: NestJS API for device communication and data storage
- **CI/CD & hosting**: GitHub Actions, Coolify
- **Hardware**: ESP32 microcontrollers + various environmental sensors
