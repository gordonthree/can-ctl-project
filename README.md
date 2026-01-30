# CAN-CTL Project Goals

A scratchpad for my sprawling CAN bus control project.

## Endpoints: Modules, nodes and controllers
 * Support STM32 and ESP32 devices
   * STM32G0B1 family
   * ESP32-S or ESP32-C family
 * Firmware to be customized to role and platform by build flags
 * PDM - Power distribution modules - control loads with switches
   * Mainly smart high-side switches from Infineon
   * Low side switching using protected MOSFets
   * eFuse Current monitoring through the smart switch or board mount sensors
 * LCM - Lighting control module - control specialized lighting loads
   * Multicolor including RGB / RGBW light modules and PWM LED strips
   * Addressable LEDs such as WS2811 or SK6812
 * MIOM - Multi IO Module - Interface with external electrical sources
   * Inputs and outputs protected against reasonable voltages and mis-connection attempts
   * Analog inputs for reading voltages, temperatures, liquid levels
   * Digital bus for interface with I2C and One-wire sensors
     * GPS and IMU
     * Environmental - Temp, pressure, humidity, CO2
     * Light level
     * Digital liquid level sensor
     * Battery SOC tracker
   * Digital inputs for contact-closures type inputs
   * Digital outputs for remote device control eg charge controller on/off
 * IFACE - Interface Modules
   * Keypads and button boxes
     * Silicone ARGB tactile keypads
     * Touchscreen type (CYD / Nextion)
     * Mechanical switches - key, toggle, momentary 
   * Displays - Simple LCD and LED readouts
 * Manager / Control firmware for ARM64, likely Raspberry Pi
 * End