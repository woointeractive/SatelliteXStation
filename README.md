# Satellite X Station
Portable Navigation System, a smart device for [Satellite X](https://apps.apple.com/app/id1520253302).

  
  

## Table of contents
- [1. Features and Screenshots](#1-features-and-screenshots)
- [2. Board and Parts](#2-board-and-parts)
- [3. Design Pictures](#3-design-pictures)
- [4. Pin Table](#4-pin-table)
- [5. Drivers](#5-drivers)
- [6. Firmwares](#6-firmwares)
- [7. App Download](#7-app-download)
  


#### **1. Features and Screenshots:**

Device:
- Search satellites automaticly
- Display active satellites
- Display current location with longitude and latitude
- Display current speed and altitude
- Display date and time in UTC timezone from  satellites
- Bluetooth mode (transfer data to App)

    ![](/images/v1.0.0_Device_1.png)
    ![](/images/v1.0.0_Device_2.png)
    ![](/images/v1.0.0_OLED.png)
  

App:
- Display longitude and latitude
- Display compass with magnetic heading
- Display pressure
- Display altitude, relative altitude
- Display pitch, roll, yaw
- Display map view, following with heading
- Display location with city and country
- GPS & BDS (Bei Dou) navigation system supported

    ![](/images/v1.x_App_1.png)
    ![](/images/v1.x_App_2.png)
    ![](/images/v1.x_App_3.png)
    ![](/images/v1.x_App_4.png)


#### **2. Board and Parts:**

- Arduino [Uno](https://store.arduino.cc/usa/arduino-uno-rev3) or [Nano](https://store.arduino.cc/usa/arduino-nano)
- Optional Shield: Uno with Arduino Sensor Shield v5, Nano with I/O Shield
- Bluetooth with CC2541 (VCC, GND, TX, RX)
- OLED Screen 128x64 IIC(I2C) with SSD1306 (VCC, GND, SDA, SCL)
- Touch button with TTP223, change deivce between on-device and bluetooth working mode (VCC, GND, IO)
- Lithium battery (3.7v, 4000+mah)
- GPS/BDS module with active antenna (VCC, GND, TX, RX)
- Type-C lithium battery charger with TP4056 (OUT+, OUT-, B+, B-)
  


#### **3. Design Pictures:**

- **Arduino Uno**

    ![](/images/v1.0.0_Uno.png)

- **Arduino Nano**

    ![](/images/v1.0.0_Nano.png)
  


#### **4. Pin Table:**

Arduino Uno / Nano Pin | Part Pin | Part Name |
:-: | :-: | :-: |
VCC | VCC | Bluetooth |
GND | GND | Bluetooth |
RX | TX | Bluetooth |
TX | RX | Bluetooth |
VCC | VCC | OLED |
GND | GND | OLED |
A4 | [SDA](https://www.arduino.cc/en/Reference/Wire) | OLED |
A5 | [SCL](https://www.arduino.cc/en/Reference/Wire) | OLED |
3.3v | 3.3v | GPS/BDS |
GND | GND | GPS/BDS |
D10 | TX | GPS/BDS |
D11 | RX | GPS/BDS |
D12 | IO | Touch |
VCC | VCC | Touch |
GND | GND | Touch |
VCC | OUT+ | Charger |
GND | OUT- | Charger |

Charger Pin | Battery Pin |
:-: | :-: |
B+ | VCC |
B- | GND |


#### **5. Drivers:**

- [macOS](https://github.com/woointeractive/Arduino/blob/master/drivers/CH34x_Install_V1.5.pkg) - Serial port driver for Sierra (10.12) and High Sierra (10.13)
  

#### **6. Firmwares:**

- [v1.0.0](/firmwares/SatelliteXStatio_v1.0.0.hex.zip)


Steps:
1. Unzip the firmware file
2. Download [Ardukit](https://apps.apple.com/app/ardukit/id1518175697) (macOS) and select .hex file to flash into Arduino board

#### **7. App Download:**

- [Satellite X](https://apps.apple.com/app/id1520253302) (Available on App Store, for iPhone, iPad)
