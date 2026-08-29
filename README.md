# DH-BTK-0
Bluetooth keyboard HID device.

Made this so I can have a wireless keyboard while practicing with ESP-IDF BLE. Split would have given me the opportunity to work with peripheral bluetooth and non-HID communications, something I have never done before.

This is an ESP32-C6 based split keyboard using RMK rust mechanical keyboard firmware. Because Zephyr RTOS support for the ESP32-C6 is limited, ZMK firmware is not a viable choice for this project, as the HID (human interface) over GATT protocol has been documented to have conflicts between NimBLE and proprietary Espressif BLE controllers. RMK uses TrouBLE, a rust-based BLE host stack for bluetooth general functionality, which allows for direct interface with esp-radio, taking the role of the connecting link between TrouBLE and the internal host controller interface for bluetooth.
CAD:
https://cad.onshape.com/documents/5130b07b114bfbcc5cc3532d
<img width="1413" height="547" alt="image" src="https://github.com/user-attachments/assets/836486c5-e64e-4d96-9f52-ba65c71e881c" />

PCB/Schematic:
<img width="1299" height="789" alt="image" src="https://github.com/user-attachments/assets/e0a6f956-a0d5-4412-aa4d-4c54ee939d67" />
<img width="657" height="840" alt="image" src="https://github.com/user-attachments/assets/cd63d8e5-bd43-4a6a-a68b-788091af4443" />
(higher quality in SVG)

To make this for yourself, simply download the gerber files found in the production folder (seen as zip files) and export to your fab of choice. I used JLCPCB here. This PCB was designed to be completely double-sided and interchangeable, as to cut down on PCB manufacturing costs. Using JLCPCB's PCB fab MOQ of 5, you can make up to 2 of these keyboards given you have enough components.
