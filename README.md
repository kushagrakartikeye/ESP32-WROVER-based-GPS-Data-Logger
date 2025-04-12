# 🛰️ ESP32-WROVER GPS Logger PCB

A custom-designed, battery-powered GPS data logger built around the ESP32-WROVER-IB-N4R8. This compact board logs real-time GPS coordinates to a MicroSD card, perfect for use in UAVs, portable trackers, and outdoor logging applications.

---

  IMPORTANT NOTE: THIS PROJECT IS STILL IN DEVELOPMENT DUE TO UNAVAILIBITY OF THE PHYSICAL COMPONENTS FOR NOW, HOWEVER THE SCHEMATICS OF THE CIRCUIT IS SHARED :)

## 📦 Features

- ✅ **ESP32-WROVER-IB-N4R8** (Dual-core MCU + Wi-Fi + Bluetooth)
- ✅ **NEO-6M GPS Module** for 1 Hz position tracking
- ✅ **MicroSD card** interface over SPI for logging
- ✅ **TP4056** Li-ion battery charging circuit (with USB-C input)
- ✅ **AMS1117-3.3** regulator to power ESP32 and peripherals
- ✅ **Pushbutton interface** for manual trigger/control
- ✅ Clean routing and low-noise power delivery
- ✅ Designed in **EasyEDA**

---

## 🔋 Power Path

- **Input**: 5V USB-C via TP4056
- **Battery**: 3.7V 1100mAh Li-ion
- **Regulation**: AMS1117 drops battery to stable 3.3V
- **Average Consumption**: ~250 mA  
- **Runtime**: ~4.4 hours on full charge

---

## 🧩 Pinout & IO Usage

| Peripheral | ESP32 GPIO | Description         |
|------------|------------|---------------------|
| GPS RX     | GPIO17     | Receives GPS data   |
| GPS TX     | GPIO16     | Sends config to GPS |
| SD CS      | GPIO5      | Chip Select         |
| SD MOSI    | GPIO23     | SPI MOSI            |
| SD MISO    | GPIO19     | SPI MISO            |
| SD CLK     | GPIO18     | SPI Clock           |
| Button     | GPIO34     | Manual log trigger  |

---

## 🖼️ Media

| 📷 PCB Preview | 🖼️ Schematic Snapshot |
|----------------|------------------------|
| ![PCB](![85a37e64-ad2e-41d8-8ec5-3b488e954e7a](https://github.com/user-attachments/assets/0d4b91be-da03-428a-bee5-32ae1dbc2acd)![f63590e7b3f14d25976cb2872803aa5f](https://github.com/user-attachments/assets/55f7a8ff-5591-4b73-b33c-295511631cc7)
 ()
) |![Schematic](![d433b5c4-8367-4a77-9b2b-36b39dbae21a](https://github.com/user-attachments/assets/a63a3b58-0215-475e-8f3f-01bb109f8fec)

---

## 🛠️ How to Build

1. Clone the repo and open the `.json` file in [EasyEDA](https://easyeda.com/)
2. Order the PCB via JLCPCB or export Gerbers
3. Assemble using the provided BOM
4. Flash your GPS logging firmware to the ESP32
5. Insert formatted SD card and battery → Done!

---

## 🧠 Future Add-ons

- OLED display for live coordinates  
- MQTT-based live tracking (via Wi-Fi)  
- Web dashboard for map plotting  

---
