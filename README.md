# BLE Beacon App for Multiple Advertisement using nRF52833 Board

This repository contains an application for creating a BLE beacon with multiple advertisement sets using the nRF52833 development board from Nordic Semiconductor and Zephyr RTOS.

## Requirements

### Hardware Platforms

- **PCA**
  - nRF5340 DK (PCA10095)
  - nRF52 DK (PCA10040)
  - nRF52840 DK (PCA10056)

### Build Targets

- nrf5340dk_nrf5340_cpuapp_ns
- nrf52dk_nrf52832
- nrf52840dk_nrf52840

## Overview

The application demonstrates the use of Bluetooth advertising sets. It implements two advertising sets:

1. Non-connectable advertising with a URI to the [Nordic Semiconductor website](https://www.nordicsemi.com) in the advertising data, showcasing the Bluetooth Broadcaster role functionality (Beacon).
2. Connectable advertising with the 16-bit UUID of the Device Information GATT Service in the advertising data, showcasing the Bluetooth Peripheral role functionality.

When the application is started, it creates two advertising sets. Observing the devices with a scanner, you'll find:

- **Nordic Beacon:** Can be used to open the nRF Beacon website.
- **Nordic multi adv sets:** Can be used to establish a connection with the device.

## User Interface

- **LED 1:** Blinks with a period of two seconds with a 50% duty cycle when the main loop is running and the device is advertising.
- **LED 2:** Lit when the development kit is connected.

## Dependencies

### nRF Connect SDK Libraries

- DK Buttons and LEDs

### Zephyr Libraries

- include/kernel.h
- Bluetooth APIs:
  - include/bluetooth/bluetooth.h
  - include/bluetooth/conn.h
  - include/bluetooth/uuid.h
  - include/bluetooth/services/dis.h

## Acknowledgments

- Acknowledgment to Nordic Semiconductor for their continuous support and contributions to the development of the nRF Connect SDK.
- Acknowledgment to the Zephyr RTOS project for providing a robust and versatile platform for embedded development.
