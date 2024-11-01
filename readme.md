# Introduction

<a href="url"><img src="./statics/reCamera-1.png" height="auto" width="auto" style="border-radius:40px"></a>

## ✨ What's reCamera? 

reCamera is a combination of a **processor** and a **camera sensor**.

This combination makes reCamera a standalone system that can handle basic detection and control tasks on its own.

## 💡 Why we make reCamera? 

Today, as processors (both SOC and MCU) are becoming smaller and more powerful, it is now possible to combine the processor with camera sensors. In fact, many IPCs (IP cameras) are already using this design to accelerate AI detection on edge devices.

So today, we introduce reCamera, an open-source camera platform for everyone to play with. We have divided this project into 3 interchangeable parts:
- Core Board
- Sensor Board
- Base Board

This design allows you to easily change the interfaces and camera sensors to suit your needs. We hope that these components can be freely combined in any way.

By building this hardware platform and ecosystem, we enable other applications to grow on this platform without the need to worry about changing from one platform to another in the future.

The engineering focus on modularity, high performance, and ease of use ensures that reCamera serves as a powerful platform for developers and makers. This design streamlines complex hardware processes, allowing users to integrate vision AI capabilities into their systems efficiently and creatively. 

We've taken care of the intricate hardware work, freeing up time for user innovation. The modular design enables users to rapidly switch cameras and customize interfaces, transforming development from months to weeks only!

Join our group:

[![Discord](https://img.shields.io/discord/667044843901681675.svg?color=768AD4&label=discord&logo=https%3A%2F%2Fdiscordapp.com%2Fassets%2F8c9701b98ad4372b58f13fd9f65f966e.svg)](https://discord.gg/agHdBMYGZK)

## Core Board

| Board         | Features                           | Version Info |
| ------------- | ---------------------------------- | ------------ |
| [C1_2002w](./C1_2002/)    | eMMC <br />WIFI/BLE module <br /> OnBoard antenna <br /> External antenna connector| 1.0 |
| [C1_2002](./C1_2002/)       | eMMC <br />Extra SDIO to base board <br /> Extra UART to base board | WIP |

### 💡 C1_2002w
This core board utilized the RISC-V SOC SG2002. In addition to the on-board eMMC, there are also on-board wireless solution ready for use. The wireless module along with the on-board antenna could provides you the basic WIFI/BLE connection ability.

While the on-board antenna cannot have a good long-range performace, you could also choose to use external antenna with the IPEX connector on-board.

### ⚙️ overview
  
Up             |  Bottom
:-------------------------:|:-------------------------:
![Up](./statics/C1_2002w_Up.png)  |  ![Bottom](./statics/C1_2002w_Bottom.png)


### ⚙️ schematic

<a href="url"><img src="./statics/BTB_Connector.png" height="auto" width="auto" style="border-radius:10px"></a>

## Sensor Board

| Board         | Features                           | Latest Version                                                   |
| ------------- | ---------------------------------- | ------------------------------------------------------------ |
| [S1_OV5647](./S1_OV5647/) | 5MP  <br />Rolling Shutter | 1.0 |
| [S2_IMX335](./S2_IMX335/)     | 5MP  <br />Rolling Shutter | WIP |
| [S3_SC130GS](./S3_SC130GS/)    | 1MP <br />Global Shutter    | WIP |
----
[Sensor Driver Support List](./Sensor_Suppoeted_List.md)

### 💡 S1_OV5647
---
### ⚙️ overview

![img](./statics/S1_ov5647.png)

### ⚙️ schematic

![img](./statics/S1_ov5647_Sch.png)

### ⚙️ features:

<div>

<table ><tbody>
<tr >
    <td >SENSOR</td>
    <td class="dbon">OV5647</td>
    <td class="dbon">CMOS SIZE</td>
    <td class="dbon">1/4 inch</td>
</tr>
<tr >
    <td class="dbon">PIXELS</td>
    <td class="dbon">5MP</td>
    <td class="dbon">APERTURE</td>
    <td class="dbon">F2.4</td>
</tr>
<tr >
    <td >FOCAL LENGTL</td>
    <td class="dbon">3.89mm</td>
    <td class="dbon">FIELD OF VIEW</td>
    <td >72.9°</td>
</tr>
<tr >
    <td >DISTORTION</td>
    <td >&lt;1.5%</td>
    <td >DEPTH OF FIELD</td>
    <td >20cm ~∞</td>
</tr>
<tr >
    <td >IMAGE</td>
    <td  colspan="3">2592 x 1944 still picture resolution</td>
</tr>
<tr >
    <td >VIDEO</td>
    <td  colspan="3">1920 x 1080p @30fps, 1280 x 720p @60fps, 640 x 480p @60fps, 640 x 480p @90fps</td>
</tr></tbody>
</table>
</div>

- 4 x LED fill lights
- 1 x microphone
- 1 x speaker
- 3 x LED indicator

### 💡 S2_IMX335
### ⚙️ overview

![image](./statics/S2_IMX335_overview.png)

### ⚙️ schematic
![alt text](./statics/S2_IMX335_Sch.png)

### ⚙️ features:


<div>

<table ><tbody>
<tr >
    <td >SENSOR</td>
    <td class="dbon">IMX335</td>
    <td class="dbon">CMOS SIZE</td>
    <td class="dbon">1/2.8 inch</td>
</tr>
<tr >
    <td class="dbon">PIXELS</td>
    <td class="dbon">5MP</td>
    <td >Focusing</td>
    <td >manually focusing</td>
</tr>
<tr >
    <td >FOCAL LENGTL</td>
    <td class="dbon">3.91mm</td>
    <td class="dbon">FIELD OF VIEW</td>
    <td >106°(D) 92.6°(H) 48.6°(V)</td>
</tr>
<tr >
    <td >IMAGE</td>
    <td  colspan="3">2592 x 1944 still picture resolution</td>
</tr>
<tr >
    <td >VIDEO</td>
    <td  colspan="3">2592 × 1944p @20fps;1920 × 1080p @30fps;1280 × 720p @30fps</td>
</tr></tbody>
</table>
</div>


### 💡 S3_SC130GS

### ⚙️ overview

![image](./statics/S3_SC130GS_overview.png)

### ⚙️ schematic

Sensor Board             |  BtoB Board
:-------------------------:|:-------------------------:
![alt text](./statics/S3_Sensor_Board.png)  |  ![alt text](./statics/S3_BtoB_Board.png)



### ⚙️ features:


<div>

<table ><tbody>
<tr >
    <td >SENSOR</td>
    <td class="dbon">SC130GS</td>
    <td class="dbon">CMOS SIZE</td>
    <td class="dbon">1/2.7 inch</td>
</tr>
<tr >
    <td class="dbon">PIXELS</td>
    <td class="dbon">1.3MP</td>
    <td >Output Format</td>
    <td >RAW MONO/RGB</td>
</tr>
<tr >
    <td >Package</td>
    <td class="dbon">64 pin CLCC</td>
    <td class="dbon">Package Size</td>
    <td >13mm x 13mm</td>
</tr>
<tr >
    <td >IMAGE</td>
    <td  colspan="3"> 1280H x 1024</td>
</tr>
<tr >
    <td >VIDEO</td>
    <td  colspan="3"> 1280H x 1024 @240fps</td>
</tr></tbody>
</table>
</div>


## Base Board


| Board         | Features                           | Version Info |
| ------------- | ---------------------------------- | ------------ |
| B1_Default    | Single Port Transformer Module <br /> SD card reader <br /> Type-C port <br /> UART| 1.0 |
| B2_Vertical-mounted Type-C      | Single Port Transformer Module <br /> SD card reader <br /> Type-C port <br /> UART| 0.1 |
| B3_POE    | Power over Ethernet(POE) <br /> UART| 0.1 |
| B4_Gyro      | DC-DC converter <br /> CAN port <br /> UART | 0.1 |

### 💡 B1_Default

### ⚙️ overview

![image](./statics/B1_Default_overview.png)

### ⚙️ schematic

![img](./statics/B1_Default_sch.png)


### ⚙️ features:

- 1 x Type-C port for power input and communication.
- 1 x Single Port Transformer Module for Ethernet communication support.
- 1 x SD card reader for data storage and exchange.

### 💡 B2_Vertical-mounted Type-C

### ⚙️ overview

![images](./statics/B2_Vertical-mounted_Type-C_overview.png)

### ⚙️ schematic

![img](./statics/B2_Vertical-mounted%20Type-C.png)

### ⚙️ features:

- 1 x Type-C port for power input and communication.
- 1 x Single Port Transformer Module for Ethernet communication support.
- 1 x SD card reader for data storage and exchange.

### 💡 B3_POE

### ⚙️ overview

Up             |  Bottom
:-------------------------:|:-------------------------:
![Up](./statics/B3_POE_Upper.png)  |  ![Bottom](./statics/B3_POE_Bottom.png)


### ⚙️ schematic

![img](./statics/B3_POE_sch.png)

### ⚙️ features:

- 1 x RJ45 port for 802.3af PSE.
- 1 x UART port.

### 💡 B4_Gyro

### ⚙️ overview

![images](./statics/B4_Gyro_overview.png)

### ⚙️ schematic

![img](./statics/B4_Gyro.png)

### ⚙️ features:

- 1 x CAN port.
- 1 x Gyroscope sensor.
- 1 x UART port.


## reCamera Softwares

### [reCamera OS](https://github.com/Seeed-Studio/reCamera-OS)

This is the default buildroot system running in reCamera.

### reCamera Web

Currently remaking with Node-red Dashboard.

This is the default Web backend running in reCamera OS. It provides user with a web interface for network configuration, live view, web ssh and other security configuration.

## Related Projects

### [reCamera Gimbal](https://github.com/AllenKon/Seeed_reCamera_Gimbal)

Open source Gimbal solution made using reCamera.

![image](./statics/reCamera-Gimbal.jpg)

### reCamera Industrial 

![image](./statics/industrial.jpg)

WIP..

### [reCamera Robot Arm]()

![image](./statics/reCamera_Robot_Arm.JPG)

WIP..
