# SecureDrawer

SecureDrawer is an Arduino-based drawer security system that detects unauthorized access using an ultrasonic sensor and RFID authentication. Built with an Arduino Uno R4, MFRC522 RFID reader, ultrasonic sensor, and buzzer, the system provides a simple and effective way to monitor a drawer and alert users when it is opened without authorization.

The system establishes a baseline distance when initialized. By continuously comparing the current distance reading to the baseline, it can detect when the drawer has been opened. If an unauthorized opening is detected, the buzzer sounds an alarm.

Authorized users can scan a registered RFID card or tag to temporarily disable the security system for 15 seconds, allowing the drawer to be opened without triggering the alarm.

## Features

* RFID-based authentication using the MFRC522 module
* Ultrasonic distance monitoring for drawer position detection
* Audible alarm for unauthorized access attempts
* Automatic baseline calibration on startup
* 15-second authorized access window after RFID verification
* Built on the Arduino Uno R4 platform

## Hardware Used

* Arduino Uno R4
* MFRC522 RFID Reader
* HC-SR04 Ultrasonic Sensor
* Piezo Buzzer
* Jumper Wires

## How It Works

1. The system records the drawer's closed position as a baseline distance.
2. The ultrasonic sensor continuously monitors the drawer position.
3. If the measured distance changes significantly, the system determines that the drawer has been opened.
4. If no authorized RFID scan has occurred, the buzzer alarm is activated.
5. Scanning a registered RFID tag temporarily disables the alarm system for 15 seconds, allowing authorized access.

## Purpose

This project was created as a fun introduction to embedded systems, sensor integration, and basic physical security concepts using Arduino.

