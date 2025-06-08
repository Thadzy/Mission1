# Mission1 – Mobile Robot Controller with ESP32 on web server

**Mission1** is a simple and effective ESP32-based web server project that allows users to remotely control GPIO pins using a browser interface. Designed as a controller module for mobile robots, it can toggle actuators, LEDs, or relays connected to GPIO 26 and GPIO 27, all over Wi-Fi.

---

## Features

* Web-based interface for controlling GPIO 26 and GPIO 27
* Real-time GPIO state monitoring
* Responsive HTML/CSS control panel
* Lightweight and self-contained HTTP server running on ESP32
* Designed for remote control of robot peripherals or modules

---

## Hardware Requirements

* ESP32 development board
* Access to a 2.4GHz Wi-Fi network
* Actuators (motors, LEDs, or relays) connected to GPIO 26 and GPIO 27
* USB cable for programming the ESP32
* Optional: Mobile robot chassis for deployment

---

## Software Requirements

* Arduino IDE (or PlatformIO)
* ESP32 board support installed via the Arduino Board Manager
* No external libraries required beyond standard Wi-Fi support

---

## How It Works

1. ESP32 connects to a predefined Wi-Fi network.
2. The board sets up a web server on port 80.
3. A client (browser) connects to the ESP32 using its local IP.
4. The web interface allows toggling GPIO 26 and GPIO 27 between `ON` and `OFF`.
5. Clicking a button sends an HTTP GET request to the ESP32 server to change the GPIO state.
6. GPIO states are reflected on the interface in real-time.

---

## Setup

1. Update your Wi-Fi credentials:

```cpp
const char* ssid = "Your_SSID";
const char* password = "Your_PASSWORD";
```

2. Connect GPIO 26 and GPIO 27 to the components you want to control.
3. Upload the code to your ESP32 using the Arduino IDE.
4. Open the Serial Monitor at 115200 baud to view the IP address.
5. Enter the IP address in a web browser to access the control interface.

---

## Web Interface

The generated web page includes:

* Current GPIO states
* ON/OFF buttons for both GPIO 26 and 27
* Responsive and accessible design with basic CSS styling

---

## Example Use Cases

* Remotely turning on/off a robot's left/right motors
* Controlling auxiliary devices (lights, arms) on a robot
* Testing GPIO control before full automation

---

## Project Structure

```
Mission1/
├── mission1_robot_control.ino   # Main Arduino sketch
├── README.md                    # Project documentation
```

---

## Notes

* Make sure to use a stable power supply for the ESP32, especially if driving motors or relays.
* Adjust GPIO pins and logic as needed for your specific motor controller or driver ICs.
* Future extensions could include:

  * Speed control using PWM
  * Real-time telemetry over WebSocket
  * Mobile-friendly design

---

## License

This project is open-source and licensed under the MIT License. You are free to use, modify, and distribute it.

---

## Credits

Built using ESP32 and Arduino framework
Inspired by foundational tutorials from Rui Santos at [Random Nerd Tutorials](https://randomnerdtutorials.com)

---

