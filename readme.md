# Smart Home Energy Management System API



[Image of smart home system architecture diagram]


## Project Overview
This project implements a simulated Smart Home Energy Management System designed to optimize power consumption using Finite State Machines (FSM). By analyzing real-time environmental data (temperature, light levels, and occupancy), the system intelligently controls HVAC (Air Conditioning) and lighting systems to reduce energy waste while maintaining user comfort.

## System Architecture & Team Roles
The system is built on a modular Python architecture, utilizing the Observer pattern for sensor-to-controller communication and a Flask REST API for simulation control and data retrieval.

* **`app.py` (Oloyede):** The core Flask API. Handles simulation routing, state evaluation, and integrates the control logic with the database.
* **`database.py` (Afolabi):** The persistence layer. Logs sensor readings and state transitions to SQLite, and computes daily energy consumption (kWh).
* **`sensors.py` & `control.py` (Anu & Ridwanullah):** The physical simulation layer. Contains the simulated environment sensors (PIR, LDR, Temperature) and the FSM logic for appliance control.

---

## Prerequisites
* Python 3.8+
* Flask (`pip install Flask`)
* Requests (`pip install requests` - for running the automated simulation script)

## Setup and Installation
1. Clone the repository to your local machine.
2. Ensure all module files (`app.py`, `database.py`, `sensors.py`, `control.py`) are located in the same root directory.
3. Install the required Python packages:
   ```bash
   pip install Flask requests
   Start the Flask server:

Bash

python app.py
The server will start running on http://127.0.0.1:5000.