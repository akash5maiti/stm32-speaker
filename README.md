# stm32-speaker
#trying create a speaker with stm32 microcontroller

Portable Bluetooth Speaker with FM Radio using STM32
This project involves the design and implementation of a portable Bluetooth speaker with FM radio functionality using an STM32 microcontroller. The speaker is designed to be efficient, compact, and user-friendly, incorporating features such as heat control and battery management for portability.

Features
Bluetooth Audio Playback
FM Radio Reception
Integrated Audio Amplifier
Battery Management System for Portability
Heat Management for Efficient Cooling
Optional LCD Display for Status Indication
Components
Microcontroller: STM32F103 or similar
Bluetooth Module: CSR8645 or similar
FM Radio Module: TEA5767 or RDA5807M
Audio Amplifier Module: TPA3116D2 or PAM8403
Speakers: 3W to 5W, 4Ω or 8Ω
Power Supply: 5V USB power supply or a rechargeable battery pack
Buttons: For control (play, pause, volume, etc.)
Resistors, Capacitors, and Connectors: For connections and filtering
LCD Display (Optional): For displaying mode and status
Circuit Design
The circuit integrates all the components mentioned above to create a functional Bluetooth speaker with FM radio. Here is a high-level schematic overview:

Schematic Overview
Power Supply:

5V Power Supply to power all modules.
Lithium-ion battery pack with BMS for portability.
USB port for charging.
Microcontroller Connections:

Bluetooth Module:
VCC to 5V
GND to Ground
Audio Out (L/R) to Audio In of the Amplifier.
FM Radio Module:
VCC to 5V
GND to Ground
SDA and SCL to I2C pins of the STM32 (e.g., PB6 and PB7 for I2C1).
Audio Out to Audio In of the Amplifier.
Antenna connection to improve reception.
Audio Amplifier Module:
VCC to 5V
GND to Ground
Audio In from Bluetooth/FM.
Audio Out to Speakers.
Buttons:
Connect buttons to GPIO pins on the STM32 for control (e.g., PA0 for Play/Pause, PA1 for Next, PA2 for Previous).
LCD Display (Optional):
Connect to I2C or SPI pins on STM32 for status display.
Heat Control:

Heat sinks on the audio amplifier.
Ventilation holes in the enclosure.
Portability:

Lithium-ion battery pack with BMS.
USB charging port.
Firmware
The firmware is written in C using the STM32CubeMX and HAL library. It includes the initialization of peripherals and implements basic functionality for switching between Bluetooth and FM modes. Additionally, it handles battery status monitoring for power management.
