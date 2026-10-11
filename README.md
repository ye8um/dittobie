# dittobie

# Dittobie
### An Interactive Digital Desk Pet

Dittobie is a small, interactive digital pet inspired by Ditto from Pokémon. Built around the Seeed Studio XIAO ESP32-C3, Dittobie combines embedded programming, custom PCB design, pixel art, motion sensing, and 3D printing to create a personalized desk companion.

The goal of this project is to bring a simple virtual pet to life through animations, physical buttons, and motion-based interactions.

---


<img width="1211" height="701" alt="image" src="https://github.com/user-attachments/assets/630b8748-b423-4484-ad40-b9173d857c2b" />


---

## Features

- **Animated Pet Display:** Displays a custom pixel-art character on a 128×64 OLED screen.
- **Idle Animation:** Uses multiple animation frames to give Dittobie more personality.
- **Motion Detection:** Uses an MPU6050 sensor to detect movement and shaking.
- **Tilt-Based Menu:** Allows the user to navigate menu options by tilting the device.
- **Interactive Actions:** Includes NAP, PLAY, EAT, and PET menu options.
- **Sleep Animation:** Displays a sleeping sprite and floating Zs while Dittobie naps.
- **Physical Controls:** Uses two buttons to access the action menu and pet statistics.
- **Custom Electronics:** Uses a custom PCB to organize and connect the components.

---

## Hardware

| Component | Purpose |
|---|---|
| Seeed Studio XIAO ESP32-C3 | Main microcontroller |
| 0.96-inch OLED display | Displays the pet and interface |
| MPU6050 | Motion and tilt detection |
| DHT11 sensor | Temperature and humidity sensing |
| 2× MX-style mechanical switches | Physical button inputs |
| Custom PCB | Connects and supports the electronics |

## KiCad PCB layout.

<img width="941" height="507" alt="image" src="https://github.com/user-attachments/assets/74a652f2-c77a-4283-9afa-0ac0ca0cd5a7" />

<img width="752" height="596" alt="image" src="https://github.com/user-attachments/assets/8f48c5db-efd6-42d5-88fc-a7a7782e33bf" />


## Software and Tools

- Arduino IDE
- C++ and the Arduino framework
- OLED display and MPU6050 libraries
- KiCad for schematic and PCB design
- Onshape for 3D modeling, if needed

---

## Pin Configuration

The current firmware uses the following pin assignments on the XIAO ESP32-C3.

| Component | Signal | Pin |
|---|---|---|
| OLED display | SDA | D4 / GPIO6 |
| OLED display | SCL | D5 / GPIO7 |
| MPU6050 | SDA | D4 / GPIO6 |
| MPU6050 | SCL | D5 / GPIO7 |
| DHT11 | Data | D1 / GPIO3 |
| Menu button | Input | D2 / GPIO4 |
| Stats button | Input | D3 / GPIO5 |


## How It Works

Dittobie uses the XIAO ESP32-C3 to process button inputs and motion sensor data while updating the OLED display.

The OLED displays the pet's sprite and animations. The MPU6050 detects movement and tilt, allowing the user to interact with the pet. The two physical buttons provide access to the action menu and statistics screen.

The menu includes four actions:

- **NAP:** Puts Dittobie into a timed sleeping state.
- **PLAY:** Provides a play interaction.
- **EAT:** Provides a feeding interaction.
- **PET:** Provides a petting interaction.

The firmware also includes a basic idle animation to make the character feel more alive.

---
