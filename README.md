# CAN-CTL Project Goals

A scratchpad for my sprawling CAN bus control project.

## Endpoints: Modules, nodes and controllers
 * Support STM32 and ESP32 devices
   * <a href="https://www.st.com/en/evaluation-tools/nucleo-g0b1re.html">STM32G0B1 family</a>
   * ESP32-WROOM, -S or -C family
 * Firmware can be customized to role and platform by build flags
 * PDM - Power distribution modules - control loads with switches
   * Mainly smart high-side switches from Infineon
   * Low side switching using protected MOSFets
   * eFuse Current monitoring through the smart switch or board mount sensors
 * LCM - Lighting control module - control specialized lighting loads
   * Multicolor including RGB / RGBW light modules and PWM LED strips
   * Addressable LEDs such as WS2811 or SK6812
 * MIOM - Multi IO Module - Interface with external electrical sources
   * Inputs and outputs protected against reasonable voltages and mis-connection attempts
   * Analog inputs for reading current transducers, voltages, temps, etc
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
     * Touchscreen type (CYD LVGL / Nextion)
     * Mechanical switches - key, toggle, momentary 
     * Multi-axis such as joypad / joystick / jog dial
   * Displays - Simple LCD and LED readouts
 * GATE - Gateway modules
   * ESP32 CAN to WiFi 
     * CAN to MQTT
     * Home Assistant
 * MGR - Manager / Controller
   * ARM64 - Raspberry Pi Based
     * Home Assistant?
     * Python?
     * Web based "touchscreen" and "gauge clusters"

## Hardware:
* <a href="https://github.com/gordonthree/SW-SMART-SIX-HIGH">Smart six-way high side switch</a>
* <a href="https://github.com/gordonthree/CAN-MULTI-IO-STM32">MultiIO node</a>
* <a href="https://github.com/gordonthree/CAN-CTL-LIGHTING-STM32">Interior Lighting Controller</a>