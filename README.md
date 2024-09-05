Smart Home System using Raspberry Pi Zero
Introduction
This project demonstrates a simple smart home system using a Raspberry Pi Zero, LEDs, a buzzer, and a photoresistor. The system allows you to control devices based on ambient light levels using Blynk for remote control through a mobile app.

Prerequisites
Hardware
Raspberry Pi Zero W
Breadboard
LEDs (Red, Green, Blue)
Resistors (220Ω, 330Ω, 1KΩ)
NPN Transistor (PN2222)
Active Buzzer
Photoresistor
Jumper Wires
MCP3008 or another ADC (if using analog sensors)
Power Supply for Raspberry Pi
Software
Raspberry Pi OS (Lite)
Python 3
Blynk Library for Python
RPi.GPIO library
Spidev library (if using MCP3008 for ADC)
Installation
Set up Raspberry Pi and install the necessary libraries:

bash
Code kopieren
sudo apt update
sudo apt install python3-pip python3-rpi.gpio python3-spidev
Install Blynk library:

bash
Code kopieren
pip3 install blynk-library-python
Clone the repository:

bash
Code kopieren
git clone https://github.com/yourusername/smart-home-system.git
cd smart-home-system
Set up your Blynk project:

Download the Blynk app on your mobile device.
Create a new project and add widgets (e.g., buttons, sliders) to control the LEDs and buzzer.
Copy the Blynk authentication token.
Update the Blynk token in the Python script:

Open Automation.py and paste your Blynk token where indicated.
Run the automation script:

bash
Code kopieren
python3 Automation.py
Circuit Setup
LED and Buzzer Connections:
Connect the Red LED to GPIO 18 via a 220Ω resistor.
Connect the Green LED to GPIO 23 via a 330Ω resistor.
Connect the Blue LED to GPIO 24 via a 1KΩ resistor.
Connect the Buzzer to GPIO 25.
Connect the Photoresistor to GPIO 27 (through ADC if used).
Breadboard Layout:
Refer to the images below for the breadboard setup:


Features
LED Control: LEDs can be controlled via the Blynk app based on the ambient light level.
Buzzer Alarm: The buzzer can be triggered via the Blynk app or automatically if the light level drops below a certain threshold.
Light Monitoring: Monitor light levels using a photoresistor and view the data in the Blynk app.
Usage
Running the Script:

After setting up the circuit and the Raspberry Pi, run the automation script:
bash
Code kopieren
python3 Automation.py
Blynk Control:

Open the Blynk app on your mobile device.
Use the widgets you set up to control the LEDs and buzzer, and monitor the light levels.
Pin Connections
GPIO 18: Red LED
GPIO 23: Green LED
GPIO 24: Blue LED
GPIO 25: Buzzer
GPIO 27: Photoresistor (through ADC)
License
This project is licensed under the MIT License - see the LICENSE file for details.
