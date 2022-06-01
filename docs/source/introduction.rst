Hardware Introduction
=======================

This document is based on EM3288 V7(MINI3288 version: V4).

1 Introduction
---------------

1.1 Summary
^^^^^^^^^^^^

  EM3288 is based on the Rockchip RK3288, Quad Core Cortex-A17 @1.8GHz.
  RK3288 is powerful on multithreaded computing operation, graphics
  processing and video decoding ability. RK3288 supports Mali-T760 MP4
  Graphics Processing, OpenGL ES1.1/2.0/3.0, OpenVG1.1, OpenCL,
  Directx11, and can 4Kx2K achieve 4kx2k H.264 and 10 bits of H.265
  video decoding, 500% performance boost over Mali-400. On display
  aspects, RK3288 supports up to 18Gbps Data transmission rate and
  4Kx2K @60Hz Video resolution.
  
1.2 Rockchip RK3288 Features
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

-  CPU

Quad-Core Cortex-A17, up to 1.8GHz

-  GPU

Mali-T764 GPU, Supports AFBC (ARM Frame Buffer Compression)

 - Support OpenGL ES 1.1/2.0/3.1, OpenCL, DirectX9.3
 - High performance dedicated 2D processor

-  Multi-image

4K 10bits H265/H264 video decoders

 - 1080P other video decoders (VC-1, MPEG-1/2/4, VP8)
 - 1080P video encoder for H.264 and VP8
 - Video post processor: de-interlace, de-noise, enhancement for
   edge/detail/color

-  Display

Support RGB/Dual LVDS/Dual MIPI-DSI/eDP interface, up to 3840*2160 resolution
HDMI 2.0 for 4K @60Hz with HDCP 1.4/2.2

-  Security
ARM TrustZone (TEE), Secure Video Path, Cipher Engine, Secure boot

-  Memory

 - Dual-channel 64bit DDR3-1333/DDR3L-1333/LPDDR2-1066
 - Support MLC NAND, eMMC 4.51
 
-  Connectivity

 - Embedded 13M ISP, MIPI CSI-2 and DVP interface
 - Dual SDIO 3.0 interface
 - TS in/CSA2.0, support DTV function
 - Embed HDMI, Ethernet MAC, S/PDIF, USB, I2C, I2S, UART, SPI, PS2

1.3 EM3288 Specifications
^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. image:: image/EM3288_SBC_Interfaces.gif
    :align: center
    
+---------------+------------------------------------------------------+
|   Feature     |   Specifications                                     |
+===============+======================================================+
| CPU           | · Rockchip RK3288, Quad Core Cortex-A17 @ 1.8GHz     |
|               |                                                      |
|               | · 28nm HKMG process                                  |
+---------------+------------------------------------------------------+
| GPU           | · ARM Mali-T764 GPU, with TE, ASTC, AFBC technology  |
|               |                                                      |
|               | · Support OpenGL ES1.1/2.0/3.0, OpenVG1.1, OpenCL,   |
|               | DirectX11                                            |
+---------------+------------------------------------------------------+
| Memory        | 512MB/1GB/2GB DDR3                                   |
+---------------+------------------------------------------------------+
| Storage       | – 4/8/16/32GB eMMC Flash                             |
|               |                                                      |
|               | – 1x SATA                                            |
|               |                                                      |
|               | – 1 x Micro SD                                       |
+---------------+------------------------------------------------------+
| Power Supply  | 5V/3A                                                |
+---------------+------------------------------------------------------+
| USB           | 3x USB2.0 Host, 1x USB2.0 OTG                        |
+---------------+------------------------------------------------------+
| Video I/O     | – HDMI 2.0 up to 3840×2160@60p                       |
|               |                                                      |
|               | – 40-pin header for LVDS (multiplexed with VGA)      |
|               |                                                      |
|               | – VGA                                                |
|               |                                                      |
|               | – 40-pin FPC connector for TTL LCD                   | 
|               |                                                      |
|               | – 26-pin header for MIPI Camera                      |
+---------------+------------------------------------------------------+
| Audio I/O     | – HDMI                                               |
|               |                                                      |
|               | – 3.5mm jacks for Audio out and Line in              |
|               |                                                      |
|               | – Differential MIC                                   |
|               |                                                      |
|               | ES8388 audio codec                                   |
+---------------+------------------------------------------------------+
| Debugging     | Serial console via 3-pin header                      |
+---------------+------------------------------------------------------+
| Connectivity  | – Gigabit Ethernet. RTL8211E-VB-CG controller        |
|               |                                                      |
|               | – Optional 802.11b/g/n and Bluetooth4.0              |
|               |                                                      |
|               | – Optional 4G Module (Built-in GPS) and SIM card slot|
|               |                                                      |
|               | – Optional GPS model via SATES (HK) ST-91-U7         |
+---------------+------------------------------------------------------+
| Expansion     | 1x 40-pin header for GPIOs, ADC, I2C, etc.           |
| Headers       |                                                      |
+---------------+------------------------------------------------------+
| Misc          | RTC, power and recovery buttons                      |
+---------------+------------------------------------------------------+
| Dimension     | 117.5 x 175.3mm                                      |
+---------------+------------------------------------------------------+

1.4 PCB Dimension
^^^^^^^^^^^^^^^^^^^

.. image:: image/2-EM3288_PCB_dimension.png
    :align: center
    
1.5 Block Diagram
^^^^^^^^^^^^^^^^^^^^

.. image:: image/3-EM3288_Block_diagram.png
    :align: center
    
1.6 CPU Introduction 
^^^^^^^^^^^^^^^^^^^^^^

.. image:: image/MINI3288.gif
   :alt: MINI3288
   :align: center
    
**Board Dimension**

| \* Board size: 70mm x 58mm
| \* Pin to Pin space: 1.3mm
| \* Pin number: (J11+J12) x 100 = 200 pins
| \* Layer: 8 Layers, complying with EMS/EMI

**Pin Definition**

+---+-----------+----+-------------+----+-----------+----+----------+
| J1                               | J2                             |
+---+-----------+----+-------------+----+-----------+----+----------+
|Pin| Signal    | Pin| Signal      | Pin| Signal    | Pin| Signal   |
+===+===========+====+=============+====+===========+====+==========+
| 1 | TX_C      | 51 | MIP         | 1  | VCC_SYS   | 51 | SPI0_U   |
|   |           |    | I_TX/RX_D2P |    |           |    | ART4_RXD |
+---+-----------+----+-------------+----+-----------+----+----------+
| 2 | TX_0-     | 52 | MIP         | 2  | GND       | 52 | SPI0_U   |
|   |           |    | I_TX/RX_D1P |    |           |    | ART4_TXD |
+---+-----------+----+-------------+----+-----------+----+----------+
| 3 | TX_C+     | 53 | MIP         | 3  | VCC_SYS   | 53 | GND      |
|   |           |    | I_TX/RX_D3P |    |           |    |          |
+---+-----------+----+-------------+----+-----------+----+----------+
| 4 | TX_0+     | 54 | GND         | 4  | GND       | 54 | TS0_SYNC |
+---+-----------+----+-------------+----+-----------+----+----------+
| 5 | GND       | 55 | MIP         | 5  | nRESET    | 55 | UA       |
|   |           |    | I_TX/RX_D3N |    |           |    | RT1_CTSn |
+---+-----------+----+-------------+----+-----------+----+----------+
| 6 | GND       | 56 | DVP_PWR     | 6  | MDI0+     | 56 |UART1_RTSn|
+---+-----------+----+-------------+----+-----------+----+----------+
| 7 | TX_1-     | 57 | HSIC_STROBE | 7  | MDI1+     | 57 | UART1_R  |
|   |           |    |             |    |           |    | X_TS0_D0 |
+---+-----------+----+-------------+----+-----------+----+----------+
| 8 | TX_2-     | 58 | HSIC_DATA   | 8  | MDI0-     | 58 | UART1_TX |
+---+-----------+----+-------------+----+-----------+----+----------+
| 9 | TX_1+     | 59 | GND         | 9  | MDI1-     | 59 | TS0_CLK  |
+---+-----------+----+-------------+----+-----------+----+----------+
| 10| TX_2+     | 60 | CIF_D1      | 10 | IR_INT    | 60 | TS0_VALID|
+---+-----------+----+-------------+----+-----------+----+----------+
| 11| HDMI_HPD  | 61 | CIF_D0      | 11 | MDI2+     | 61 | TS0_ERR  |
+---+-----------+----+-------------+----+-----------+----+----------+
| 12| HDMI_CEC  | 62 | CIF_D3      | 12 | MDI3+     | 62 |GPIO7_B4_U|
+---+-----------+----+-------------+----+-----------+----+----------+
| 13| I2C5      | 63 | CIF_D2      | 13 | MDI2-     | 63 | S        |
|   | _SDA_HDMI |    |             |    |           |    | DMMC_CLK |
+---+-----------+----+-------------+----+-----------+----+----------+
| 14| I2C5      | 64 | CIF_D5      | 14 | MDI3-     | 64 | GND      |
|   | _SCL_HDMI |    |             |    |           |    |          |
+---+-----------+----+-------------+----+-----------+----+----------+
| 15| GND       | 65 | CIF_D4      | 15 | GND       | 65 | SDMMC_D0 |
+---+-----------+----+-------------+----+-----------+----+----------+
| 16| LCD_VSYNC | 66 | CIF_D7      | 16 | RST_KEY   | 66 | SDMMC_CMD|
+---+-----------+----+-------------+----+-----------+----+----------+
| 17| LCD_HSYNC | 67 | CIF_D6      | 17 | SDIO0_CMD | 67 | SDMMC_D2 |
+---+-----------+----+-------------+----+-----------+----+----------+
| 18| LCD_CLK   | 68 | CIF_D9      | 18 | SDIO0_D0  | 68 | SDMMC_D1 |
+---+-----------+----+-------------+----+-----------+----+----------+
| 19| LCD_DEN   | 69 | CIF_D8      | 19 | SDIO0_D1  | 69 | SDMMC_DET|
+---+-----------+----+-------------+----+-----------+----+----------+
| 20|LCD_D0_LD0P| 70 | CIF_PDN0    | 20 | SDIO0_D2  | 70 | SDMMC_D3 |
+---+-----------+----+-------------+----+-----------+----+----------+
| 21|LCD_D1_LD0N| 71 | CIF_D10     | 21 | SDIO0_D3  | 71 | SDMMC_PWR|
+---+-----------+----+-------------+----+-----------+----+----------+
| 22|LCD_D2_LD1P| 72 | CIF_HREF    | 22 | SDIO0_CLK | 72 |GPIO0_B5_D|
+---+-----------+----+-------------+----+-----------+----+----------+
| 23|LCD_D3_LD1N| 73 | CIF_VSYNC   | 23 | BT_WAKE   | 73 | GND      |
+---+-----------+----+-------------+----+-----------+----+----------+
| 24|LCD_D4_LD2P| 74 | CIF_CLKOUT  | 24 | SDIO0_WP  | 74 |GPIO7_B7_D|
+---+-----------+----+-------------+----+-----------+----+----------+
| 25|LCD_D5_LD2N| 75 | CIF_CLKIN   | 25 |WIFI_REG_ON| 75 | I2S_SDI  |
+---+-----------+----+-------------+----+-----------+----+----------+
| 26|LCD_D6_LD3P| 76 | I2C3_SCL    | 26 |BT_HOS     | 76 | I2S_MCLK |
|   |           |    |             |    |T_WAKE     |    |          |
+---+-----------+----+-------------+----+-----------+----+----------+
| 27|LCD_D7_LD3N| 77 | I2C3_SDA    | 27 | WIFI_H    | 77 | I2S_SCLK |
|   |           |    |             |    | OST_WAKE  |    |          |
+---+-----------+----+-------------+----+-----------+----+----------+
| 28| LC        | 78 | GND         | 28 | BT_RST    | 78 |I2S_L     |
|   | D_D8_LD4P |    |             |    |           |    |RCK_RX    |
+---+-----------+----+-------------+----+-----------+----+----------+
| 29| LC        | 79 | GPIO0_B2_D  | 29 | SPI2_CLK  | 79 | I2S      |
|   | D_D9_LD4N |    |             |    |           |    | _LRCK_TX |
+---+-----------+----+-------------+----+-----------+----+----------+
| 30| LCD_D10   | 80 | GPIO7_A3_D  | 30 | SP2I_CSn0 | 80 | I2S_SDO0 |
|   | _LCK0P    |    |             |    |           |    |          |
+---+-----------+----+-------------+----+-----------+----+----------+
| 31| LCD_D11   | 81 | GPIO7_A6_U  | 31 | SPI2_RXD  | 81 | 2S_SDO1  |
|   | _LCK0N    |    |             |    |           |    |          |
+---+-----------+----+-------------+----+-----------+----+----------+
| 32| LCD       | 82 | GPIO0_A6_U  | 32 | SPI2_TXD  | 82 | I2S_SDO2 |
|   | _D12_LD5P |    |             |    |           |    |          |
+---+-----------+----+-------------+----+-----------+----+----------+
| 33| LCD       | 83 | LED0_AD0    | 33 | OTG       | 83 | I2S_SDO3 |
|   | _D13_LD5N |    |             |    | _VBUS_DRV |    |          |
+---+-----------+----+-------------+----+-----------+----+----------+
| 34| LCD       | 84 | LED1_AD1    | 34 | HOST      | 84 | SPDIF_TX |
|   | _D14_LD6P |    |             |    | _VBUS_DRV |    |          |
+---+-----------+----+-------------+----+-----------+----+----------+
| 35| LCD       | 85 | VCC_LAN     | 35 | UART0_RX  | 85 | I2C2_SDA |
|   | _D15_LD6N |    |             |    |           |    |          |
+---+-----------+----+-------------+----+-----------+----+----------+
| 36| LCD       | 86 | PS2_DATA    | 36 | UART0_TX  | 86 | GND      |
|   | _D16_LD7P |    |             |    |           |    |          |
+---+-----------+----+-------------+----+-----------+----+----------+
| 37| LCD       | 87 | PS2_CLK     | 37 | GND       | 87 | I2C1_SDA |
|   | _D17_LD7N |    |             |    |           |    |          |
+---+-----------+----+-------------+----+-----------+----+----------+
| 38| LCD       | 88 | ADC0_IN     | 38 | UART0_CTS | 88 | I2C2_SCL |
|   | _D18_LD8P |    |             |    |           |    |          |
+---+-----------+----+-------------+----+-----------+----+----------+
| 39| LCD       | 89 | GPIO0_A7_U  | 39 | OTG_DM    | 89 | I2C4_SDA |
|   | _D19_LD8N |    |             |    |           |    |          |
+---+-----------+----+-------------+----+-----------+----+----------+
| 40| LCD       | 90 | ADC1_IN     | 40 | UART0_RTS | 90 | I2C1_SCL |
|   | _D20_LD9P |    |             |    |           |    |          |
+---+-----------+----+-------------+----+-----------+----+----------+
| 41| LCD       | 91 | VCCIO_SD    | 41 | OTG_DP    | 91 | UART2_RX |
|   | _D21_LD9N |    |             |    |           |    |          |
+---+-----------+----+-------------+----+-----------+----+----------+
| 42| LCD_D22   | 92 | ADC2_IN     | 42 | OTG_ID    | 92 | I2C4_SCL |
|   | _LCK1P    |    |             |    |           |    |          |
+---+-----------+----+-------------+----+-----------+----+----------+
| 43| LCD_D23   | 93 | VCC_CAM     | 43 | HOST1_DM  | 93 | UART3_RX |
|   | _LCK1N    |    |             |    |           |    |          |
+---+-----------+----+-------------+----+-----------+----+----------+
| 44| GND       | 94 | VCCA_33     | 44 | OTG_DET   | 94 | UART2_TX |
+---+-----------+----+-------------+----+-----------+----+----------+
| 45| MIPI_TX/RX| 95 | VCC_18      | 45 | HOST1_DP  | 95 | UA       |
|   | _CLKN     |    |             |    |           |    | RT3_RTSn |
+---+-----------+----+-------------+----+-----------+----+----------+
| 46| MIPI_TX/RX| 96 | VCC_RTC     | 46 | HOST2_DM  | 96 | UART3_TX |
|   | _D0P      |    |             |    |           |    |          |
+---+-----------+----+-------------+----+-----------+----+----------+
| 47| MIPI_T    | 97 | VCC_IO      | 47 | SPI0_CSn0 | 97 | PWM1     |
|   | X/RX_CLKP |    |             |    |           |    |          |
+---+-----------+----+-------------+----+-----------+----+----------+
| 48| MIPI_TX/RX| 98 | GND         | 48 | HOST2_DP  | 98 | UA       |
|   | _D0N      |    |             |    |           |    | RT3_CTSn |
+---+-----------+----+-------------+----+-----------+----+----------+
| 49|MIPI_TX/RX | 99 | VCC_IO      | 49 | SPI0_CLK  | 99 | PWR_KEY  |
|   |_D2N       |    |             |    |           |    |          |
+---+-----------+----+-------------+----+-----------+----+----------+
| 50| MIPI_TX/RX| 1  | GND         | 50 | GND       | 1  | GP       |
|   | _D1N      | 00 |             |    |           | 00 | IO7_C5_D |
+---+-----------+----+-------------+----+-----------+----+----------+

2 Peripherals 
--------------

2.1 Power (P6, J17)
^^^^^^^^^^^^^^^^^^^

EM3288 Power Supply – 5V DC power supply or external Li+ battery

-  **5V/3A DC power supply (P6)**

.. image:: image/6-DC.gif
    :align: center
    
+---+--------+---------------------------+---+--------+--------------+
|Pin| Signal | Description               |Pin| Signal | Description  |
+---+--------+---------------------------+---+--------+--------------+
| 1 | VDD5V  | Main power supply. DC 5V  | 2 | GND    | Ground       |
|   |        | power in                  |   |        |              |
+---+--------+---------------------------+---+--------+--------------+
| 3 | GND    | Ground                    |                           |
+---+--------+---------------------------+---+--------+--------------+

-  **Lithium battery (J17)**

EM3288 provides an external Li-battery interface. **It is a reserved interface.**

.. image:: image/7-DC-SATA.gif
    :align: center
    
+---+--------+----------------+---+------+---------------------------+
|Pin| Signal | Description    |Pin|Signal| Description               |
+---+--------+----------------+---+------+---------------------------+
| 1 | GND    | Ground         | 2 | VBAT | Li-Battery                |
+---+--------+----------------+---+------+---------------------------+

2.2 Ethernet (JP1)
^^^^^^^^^^^^^^^^^^^

.. image:: image/8-Ethernet.gif
    :align: center
    
RK3288 has integrated Gigabit Ethernet MAC. EM3288 adopts RTL8211E as
the Ethernet chip. RJ45 connector

**Feature**

-  Supports 10/100/1000-Mbps data transfer rates with the RGMII
   interfaces
-  Supports both full-duplex and half-duplex operation
-  Supports IEEE 802.1Q VLAN tag detection for reception frames

+---+---------+--------------------+---+--------+--------------------+
|Pin| Signal  | Description        |Pin| Signal | Description        |
+---+---------+--------------------+---+--------+--------------------+
| 1 | COM     | Common             | 2 | MDI0P  | Bi-directional     |
|   |         |                    |   |        | transmit/receive   |
|   |         |                    |   |        | pair 0             |
+---+---------+--------------------+---+--------+--------------------+
| 3 | MDI0N   | Bi-directional     | 4 | MDI1P  | Bi-directional     |
|   |         | transmit/receive   |   |        | transmit/receive   |
|   |         | pair 0             |   |        | pair 1             |
+---+---------+--------------------+---+--------+--------------------+
| 5 | MDI2P   | Bi-directional     | 6 | MDI2N  | Bi-directional     |
|   |         | transmit/receive   |   |        | transmit/receive   |
|   |         | pair2              |   |        | pair2              |
+---+---------+--------------------+---+--------+--------------------+
| 7 | MDI1N   | Bi-directional     | 8 | MDI3P  | Bi-directional     |
|   |         | transmit/receive   |   |        | transmit/receive   |
|   |         | pair 1             |   |        | pair 3             |
+---+---------+--------------------+---+--------+--------------------+
| 9 | MDI3N   | Bi-directional     | 10| GND    | Ground             |
|   |         | transmit/receive   |   |        |                    |
|   |         | pair 3             |   |        |                    |
+---+---------+--------------------+---+--------+--------------------+
| 11| VCC_LAN | 3.3V               | 12| LINK   | Detect link        |
+---+---------+--------------------+---+--------+--------------------+
| 13| GND     | Ground             | 14| SPEED  | Detect speed       |
+---+---------+--------------------+---+--------+--------------------+
| 15| GND     | Ground             | 16| GND    | Ground             |
+---+---------+--------------------+---+--------+--------------------+

2.3 USB HOST (P2, P3)
^^^^^^^^^^^^^^^^^^^

EM3288 provides 3x USB2.0 Host. One is a single USB (P2), and the other
is a double-USB (P3). The 3-ch USB HOST interfaces are extended by
AU6256 which is a fully compliant with the USB 2.0 hub specification and
is designed to work with USB host as a high-speed hub.

**Feature**

-  Compatible with USB Host2.0 specification
-  Supports high-speed (480Mbps), full-speed (12Mbps) and low-speed
   (1.5Mbps) mode
-  Supports automatic switching between bus- and self-powered modes
-  Provides 16 host mode channels
-  Support periodic out channel in host mode

.. image:: image/9-USB-AF.gif
    :align: center
    
+---+---------+--------------------+---+--------+--------------------+
| Single Host (P2)                                                   |
+---+---------+--------------------+---+--------+--------------------+
|Pin| Signal  | Description        |Pin| Signal | Description        |
+---+---------+--------------------+---+--------+--------------------+
| 1 | VCC_5V  | USB Power. DC 5V   | 2 | USB_DM2| USB data-          |
+---+---------+--------------------+---+--------+--------------------+
| 3 | USB_DP2 | USB Data+          | 4 | GND    | Ground             |
+---+---------+--------------------+---+--------+--------------------+
| 5 | GND     | Ground             | 6 | GND    | Ground             |
+---+---------+--------------------+---+--------+--------------------+
| 7 | GND     | Ground             |                                 |
+---+---------+--------------------+---+--------+--------------------+

.. image:: image/10-2xUSB-AF.gif
    :align: center
    
+---+-------------+---------------+---+--------------+--------------+
| Dual-USB Host (P3)                                                |
+---+-------------+---------------+---+--------------+--------------+
|Pin| Signal      | Description   |Pin| Signal       | Description  |
+---+-------------+---------------+---+--------------+--------------+
| 1 | VCC_USB     |USB Power. DC5V| 2 | USB_DM3      | USB data-    |
+---+-------------+---------------+---+--------------+--------------+
| 3 | USB_DP3     | USB Data+     | 4 | GND          | Ground       |
+---+-------------+---------------+---+--------------+--------------+
| 5 | VCC_USB     |USB Power. DC5V| 6 | USB_DM4      | USB data-    |
+---+-------------+---------------+---+--------------+--------------+
| 7 | USB_DP4     | USB Data+     | 8 | GND          | Ground       |
+---+-------------+---------------+---+--------------+--------------+
| 9 | GND         | Ground        | 10| GND          | Ground       |
+---+-------------+---------------+---+--------------+--------------+
| 11| GND         | Ground        | 12| GND          | Ground       |
+---+-------------+---------------+---+--------------+--------------+

2.4 USB OTG (J8)
^^^^^^^^^^^^^^^^^^^

EM3288 OTG is a Micro USB2.0 port, it is used to download image and ADB
transfer file.

**Feature**

-  Compatible with USB OTG2.0 specification
-  Supports USB 2.0 High Speed (480Mbps), Full Speed (12Mbps) and Low
   Speed (1.5Mbps) operation in host mode
-  Supports USB 2.0 High Speed (480 Mbps) and Full Speed (12 Mbps)
   operation in peripheral mode.
-  Hardware support for OTG signaling, session request protocol, and
   host negotiation protocol.

.. image:: image/11-Micro_USB.gif
    :align: center
    
+---+-------------+---------------+---+--------------+--------------+
|Pin| Signal      | Description   |Pin| Signal       | Description  |
+---+-------------+---------------+---+--------------+--------------+
| 1 | OTG_DET     | OTG detection | 2 | OTG_DM       | OTG data -   |
+---+-------------+---------------+---+--------------+--------------+
| 3 | OTG_DP      | OTG data+     | 4 | OTG_ID       | OTG ID       |
|   |             |               |   |              | indicator    |
+---+-------------+---------------+---+--------------+--------------+
| 5 | GND         | Ground        |                                 |
+---+-------------+---------------+---+--------------+--------------+

2.5 Micro SD (J1)
^^^^^^^^^^^^^^^^^^^

The Micro SD card is used as an external storage device. The MMC
controller interface supports up to 4-bit transfer modes. MMC is always
accessible through the carrier board interface. It does not support
hot-plug.

.. image:: image/12-Micro_SD.gif
    :align: center
    
+---+------------+-----------------+---+--------------+--------------+
|Pin| Signal     | Description     |Pin| Signal       | Description  |
+---+------------+-----------------+---+--------------+--------------+
| 1 | SDMMC_D2   | SD/MMC data2    | 2 | SDMMC_D3     | SD/MMC data3 |
+---+------------+-----------------+---+--------------+--------------+
| 3 | SDMMC_CMD  | SD/MMC command  | 4 | VCCIO_SD     | 3.3V         |
|   |            | signal          |   |              |              |
+---+------------+-----------------+---+--------------+--------------+
| 5 | SDMMC_CLK  | SD/MMC clock    | 6 | GND          | Ground       |
+---+------------+-----------------+---+--------------+--------------+
| 7 | SDMMC_D0   | SD/MMC data0    | 8 | SDMMC_D1     | SD/MMC data1 |
+---+------------+-----------------+---+--------------+--------------+
| 9 | SDMMC_DET  | SD/MMC detect   |                                 |
|   |            | signal          |                                 |
+---+------------+-----------------+---+--------------+--------------+

2.6 HDMI (PH1)
^^^^^^^^^^^^^^^^^^^

EM3288 HDMI2.0 supports maximum 4Kx2K display, and it also enables
HDMI/LCD audio and video synchronization output. The HDMI interface is
the regular 19pins HDMI type A, with width 13.9mm and thickness 4.45mm.

.. image:: image/13-HDMI.gif
    :align: center
    
+---+-------------+---------------+---+--------------+--------------+
|Pin| Signal      | Description   |Pin| Signal       | Description  |
+---+-------------+---------------+---+--------------+--------------+
| 1 | TX_2+       | HDMI data 2   | 2 | GND          | Ground       |
|   |             | pair          |   |              |              |
+---+-------------+---------------+---+--------------+--------------+
| 3 | TX_2-       |               | 4 | TX_1+        | HDMI data 1  |
|   |             |               |   |              | pair         |
+---+-------------+---------------+---+--------------+--------------+
| 5 | GND         | Ground        | 6 | TX_1-        |              |
+---+-------------+---------------+---+--------------+--------------+
| 7 | TX_0+       | HDMI data 0   | 8 | GND          | Ground       |
|   |             | pair          |   |              |              |
+---+-------------+---------------+---+--------------+--------------+
| 9 | TX_0-       |               | 10| TX_C+        | HDMI clock   |
|   |             |               |   |              | pair         |
+---+-------------+---------------+---+--------------+--------------+
| 11| GND         | Ground        | 12| TX_C-        |              |
+---+-------------+---------------+---+--------------+--------------+
| 13| HDMI_CEC    | Consumer      | 14| NC           | Not connect  |
|   |             | electronics   |   |              |              |
|   |             | control       |   |              |              |
+---+-------------+---------------+---+--------------+--------------+
| 15| HDMI_SCL    | HDMI serial   | 16| HDMI_SDA     | HDMI serial  |
|   |             | clock         |   |              | data         |
+---+-------------+---------------+---+--------------+--------------+
| 17| GND         | Ground        | 18| HDMI_VCC     | 5V           |
+---+-------------+---------------+---+--------------+--------------+
| 19| HDMI_HPD    |Hot Plug Detect| 20| GND          | Ground       |
+---+-------------+---------------+---+--------------+--------------+
| 21| GND         | Ground        | 22| GND          | Ground       |
+---+-------------+---------------+---+--------------+--------------+
| 23| GND         | Ground        |                                 |
+---+-------------+---------------+---+--------------+--------------+

2.7 Audio I/O (J6, J7, MIC1)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

The EM3288 adopts audio codec ES8388, provides stereo audio output
(Green, 3.5mm audio jack) and line in (Pink, 3.5mm audio jack).

**Features**

-  Low power
-  Integrated ADC and DAC
-  IIS transfer audio data
-  Stereo output, support recording

.. image:: image/14-Audio.gif
    :align: center
    
+---+------+----------------------+---+------+----------------------+
| Line in (J6)                                                      |
+---+------+----------------------+---+------+----------------------+
|Pin|Signal| Description          |Pin|Signal| Description          |
+---+------+----------------------+---+------+----------------------+
| 1 | GND  | Ground               | 2 | RIN2 | Right Channel input  |
+---+------+----------------------+---+------+----------------------+
| 3 | RIN2 | Right Channel input  | 4 | LIN2 | Left Channel input   |
+---+------+----------------------+---+------+----------------------+
| 5 | LIN2 | Left Channel input   |                                 |
+---+------+----------------------+---+------+----------------------+
| Audio out (J7)                                                    |
+---+------+----------------------+---+------+----------------------+
|Pin|Signal| Description          |Pin|Signal| Description          |
+---+------+----------------------+---+------+----------------------+
| 1 | GND  | Ground               | 2 | H    | Right Channel        |
|   |      |                      |   | P_RO | Headphone Output     |
+---+------+----------------------+---+------+----------------------+
| 3 | A    | Right Channel        | 4 | A    | Left Channel         |
|   | ROUT | Headphone Output     |   | LOUT | Headphone Output     |
+---+------+----------------------+---+------+----------------------+
| 5 | H    | Left Channel         |   |      |                      |
|   | P_LO | Headphone Output     |   |      |                      |
+---+------+----------------------+---+------+----------------------+

The Microphone MIC1 model is WM_64BC MIC/F6/DIP. It is used for
recording.

.. image:: image/15-MIC.gif
    :align: center
    
+---+-------------+---------------+---+--------------+--------------+
| MIC1                                                              |
+---+-------------+---------------+---+--------------+--------------+
|Pin| Signal      | Description   |Pin| Signal       | Description  |
+---+-------------+---------------+---+--------------+--------------+
| 1 | MIC1P       | Command signal| 2 | MIC1N        | Ground       |
+---+-------------+---------------+---+--------------+--------------+

.. Note::

   1. The audio default output from HDMI. No sound in headphone if not remove HDMI.
   2. Default recording via MIC1 if the Line_in jack is not plugged in.

2.8 VGA (J20)
^^^^^^^^^^^^^^^^^^^

EM3288 adopts standard 15-pin female VGA connector, and SDA7123
3-Channel 10 Digit Video D/A converter.

.. image:: image/16-VGA.gif
    :align: center
    
+---+------------+----------------+---+--------------+--------------+
|Pin| Signal     | Description    |Pin| Signal       | Description  |
+---+------------+----------------+---+--------------+--------------+
| 1 | IOR        | Video red      | 2 | IOG          | Video green  |
+---+------------+----------------+---+--------------+--------------+
| 3 | IOB        | Video blue     | 4 | NC           | Not connect  |
+---+------------+----------------+---+--------------+--------------+
| 5 | GND        | Ground         | 6 | GND          | Ground       |
+---+------------+----------------+---+--------------+--------------+
| 7 | GND        | Ground         | 8 | GND          | Ground       |
+---+------------+----------------+---+--------------+--------------+
| 9 | VCC5V      | DC 5V          | 10| GND          | Ground       |
+---+------------+----------------+---+--------------+--------------+
| 12| NC         | Not connect    | 12| VGA_OUT_SDA  | Serial Data  |
+---+------------+----------------+---+--------------+--------------+
| 13| LCD_HSYNC  | LCD Horizontal | 14| LCD_VSYNC    | LCD Vertical |
|   |            | Sync           |   |              | Sync         |
+---+------------+----------------+---+--------------+--------------+
| 15| GND        | Ground         |                                 |
+---+------------+----------------+---+--------------+--------------+

2.9 LVDS (CON3)
^^^^^^^^^^^^^^^^^^^

EM3288 supports 10.1-inch HD capacitive LCD, up to 1280 x 800
resolution.

**Feature**

-  Comply with the TIA/EIA-644-A LVDS standard
-  Combine LVTTL IO, support LVDS/LVTTL data output
-  Support reference clock frequency range from 10MHz to 148.5MHz
-  Support LVDS RGB 30/24/18bits color data transfer
-  Support VESA/JEIDA LVDS data format transfer
-  Support MSB mode and LSB mode data transfer

.. image:: image/17-LVDS.gif
    :align: center
    
+---+-----------+---+------------+---+------------+---+-------------+
|Pin| Signal    |Pin| Signal     |Pin| Signal     |Pin| Signal      |
+---+-----------+---+------------+---+------------+---+-------------+
| 1 | VCC5V     | 2 | VCC5V      | 3 | GND        | 4 | GND         |
+---+-----------+---+------------+---+------------+---+-------------+
| 5 | VCC_IO    | 6 | VCC_IO     | 7 | GND        | 8 | GND         |
+---+-----------+---+------------+---+------------+---+-------------+
| 9 | I2C4_SCL  | 10| I2C4_SDA   | 11| TOUCH_RST  | 12| TOUCH_INT   |
+---+-----------+---+------------+---+------------+---+-------------+
| 13| LVDS_EN   | 14| LVDS_PWM   | 15| GND        | 16| GND         |
+---+-----------+---+------------+---+------------+---+-------------+
| 17| LCK1P     | 18| LCK1N      | 19| GND        | 20| GND         |
+---+-----------+---+------------+---+------------+---+-------------+
| 21| LD8P      | 22| LD8N       | 23| LD7P       | 24| LD7N        |
+---+-----------+---+------------+---+------------+---+-------------+
| 25| LD6P      | 26| LD6N       | 27| LD5P       | 28| LD5N        |
+---+-----------+---+------------+---+------------+---+-------------+
| 29| LCK0P     | 30| LCK0N      | 31| GND        | 32| GND         |
+---+-----------+---+------------+---+------------+---+-------------+
| 33| LD3P      | 34| LD3N       | 35| LD2P       | 36| LD2N        |
+---+-----------+---+------------+---+------------+---+-------------+
| 37| LD1P      | 38| LD1N       | 39| LD0P       | 40| LD0N        |
+---+-----------+---+------------+---+------------+---+-------------+

2.10 TTL LCD (J21)
^^^^^^^^^^^^^^^^^^^

J21 is a 40-pin FPC connector for TTL LCD.

.. image:: image/18-FPC.gif
    :align: center
    
+---+-----------+---+------------+---+------------+---+-------------+
|Pin| Signal    |Pin| Signal     |Pin| Signal     |Pin| Signal      |
+---+-----------+---+------------+---+------------+---+-------------+
| 1 | VCC5V     | 2 | VCC5V      | 3 | LCD_D0_LD0P| 4 | LCD_D1_LD0N |
+---+-----------+---+------------+---+------------+---+-------------+
| 5 |LCD_D2_LD1P| 6 | CD_D3_LD1N | 7 | LCD_D4_LD2P| 8 | LCD_D5_LD2N |
+---+-----------+---+------------+---+------------+---+-------------+
| 9 |LCD_D6_LD3P| 10| LCD_D7_LD3N| 11| GND        | 12| LCD_D8_LD4P |
+---+-----------+---+------------+---+------------+---+-------------+
| 13| LC        | 14| LCD        | 15| LCD        | 16| L           |
|   | D_D9_LD4N |   | _D10_LCK0P |   | _D11_LCK0N |   | CD_D12_LD5P |
+---+-----------+---+------------+---+------------+---+-------------+
| 17| LCD       | 18| LC         | 19| LC         | 20| GND         |
|   | _D13_LD5N |   | D_D14_LD6P |   | D_D15_LD6N |   |             |
+---+-----------+---+------------+---+------------+---+-------------+
| 21| LCD       | 2 |LCD_D17_LD7N| 2 |LCD_D18_LD8P| 24| LCD_D19_LD8N|
|   | _D16_LD7P |   |            | 3 |            |   |             |
+---+-----------+---+------------+---+------------+---+-------------+
| 25| LCD       | 26| LC         | 27| LCD        | 28| LC          |
|   | _D20_LD9P |   | D_D21_LD9N |   | _D22_LCK1P |   | D_D23_LCK1N |
+---+-----------+---+------------+---+------------+---+-------------+
| 29| GND       | 30| LVDS_PWM   | 31| GND        | 32| GND         |
+---+-----------+---+------------+---+------------+---+-------------+
| 33| LCD_DEN   | 34| LCD_VSYNC  | 35| LCD_HSYNC  | 36| LCD_CLK     |
+---+-----------+---+------------+---+------------+---+-------------+
| 37| TSXM      | 38| TSXP       | 39| TSYM       | 40| TSYP        |
+---+-----------+---+------------+---+------------+---+-------------+

2.11 MIPI (CON5)
^^^^^^^^^^^^^^^^^^^

EM3288 supports MIPI Camera.

**Features**

-  Embedded 3 MIPI PHY, MIPI 0 only for TX, MIPI 1 for TX and RX, MIPI 2
   only for RX
-  Support 4 data lane, providing up to 6Gbps data rate
-  Support 1080p@60fps output
-  Lane operation ranging from 80 Mbps to 1.5Gbps in forward direction.

.. image:: image/19-mipi-Camera.gif
    :align: center
    
+---+-----------+------------------+---+-----------+-----------------+
|Pin| Signal    | Description      |Pin| Signal    | Description     |
+---+-----------+------------------+---+-----------+-----------------+
| 1 | VCC5V     | DC 5V            | 2 | VCC5V     | DC 5V           |
+---+-----------+------------------+---+-----------+-----------------+
| 3 | GND       | Ground           | 4 | GND       | Ground          |
+---+-----------+------------------+---+-----------+-----------------+
| 5 | VCC_IO    | DC 3.3V          | 6 | VCC_IO    | DC 3.3V         |
+---+-----------+------------------+---+-----------+-----------------+
| 7 | VCCA_18   | DC 1.8V          | 8 | GND       | Ground          |
+---+-----------+------------------+---+-----------+-----------------+
| 9 | LCD1_BL   | Backlight        | 10| LCD1_BL_EN| Backlight enable|
+---+-----------+------------------+---+-----------+-----------------+
| 11| CIF_CLKOUT| Camera clock     | 12| I2C3_SCL  | I2C clock line  |
+---+-----------+------------------+---+-----------+-----------------+
| 13| I2C3_SDA  | I2c date line    | 14| TOUCH_RST | Touch screen    |
|   |           |                  |   |           | reset           |
+---+-----------+------------------+---+-----------+-----------------+
| 15| TOUCH_INT | Touch screen int | 16| GND       | Ground          |
+---+-----------+------------------+---+-----------+-----------------+
| 17| CLKN      | MIPI clock -     | 18| CLKP      | MIPI clock +    |
+---+-----------+------------------+---+-----------+-----------------+
| 19| D0N       | Negative         | 20| D0P       | Positive        |
|   |           | Transmission     |   |           | Transmission    |
|   |           | Data of Pixel0   |   |           | Data of Pixel0  |
+---+-----------+------------------+---+-----------+-----------------+
| 21| D1N       | Negative         | 22| D1P       | Positive        |
|   |           | Transmission     |   |           | Transmission    |
|   |           | Data of Pixel1   |   |           | Data of Pixel1  |
+---+-----------+------------------+---+-----------+-----------------+
| 23| D2N       | Negative         | 24| D2P       | Positive        |
|   |           | Transmission     |   |           | Transmission    |
|   |           | Data of Pixel2   |   |           | Data of Pixel2  |
+---+-----------+------------------+---+-----------+-----------------+
| 25| D3N       | Negative         | 26| D3P       | Positive        |
|   |           | Transmission     |   |           | Transmission    |
|   |           | Data of Pixel3   |   |           | Data of Pixel3  |
+---+-----------+------------------+---+-----------+-----------------+

2.12 GPS (MU4)
^^^^^^^^^^^^^^^^^^^

.. image:: image/20-GPS.gif
    :align: center
    
The GPS module (Model: ST-91-U7) uses ublox 7 chipset which is high
performance u-blox 7 multi-GNSS (GPS, GLONASS, QZSS, SBAS – Galileo and
Compass ready) position engine delivers exceptional sensitivity and
acquisition times.

**Features**

-  Ublox 7 high performance and low power consumption GPS Chipset
-  Very high sensitivity (Tracking Sensitivity: -162dBm)
-  Extremely fast TTFF (Time to First Fix) at low signal level
-  Two serial port: UART, I2C
-  Built-in LNA
-  A-GPS Support
-  Exceptional jamming immunity
-  Support NMEA 0183 and ublox binary protocol
-  Channels: 56
-  Available Baud: 9,600 bps
-  The antenna band is 1575.42MHZ; Voltage: 3.0-5.0V

+---+-------------+---------------+---+--------------+--------------+
|Pin| Signal      | Description   |Pin| Signal       | Description  |
+---+-------------+---------------+---+--------------+--------------+
| 1 | GND         | Ground        | 2 | GPS_UART3_RX | UART3        |
|   |             |               |   |              | receive      |
+---+-------------+---------------+---+--------------+--------------+
| 3 | G           | UART3         | 4 | NC           | Not connect  |
|   | PS_UART3_TX | transmit      |   |              |              |
+---+-------------+---------------+---+--------------+--------------+
| 5 | NC          | Not connect   | 6 | VCC_RTC      | Backup       |
|   |             |               |   |              | voltage      |
|   |             |               |   |              | supply       |
+---+-------------+---------------+---+--------------+--------------+
| 7 | GPSVDDIO    | IO Supply     | 8 | VDD_GPS      | Supply       |
|   |             | Voltage       |   |              | voltage      |
+---+-------------+---------------+---+--------------+--------------+
| 9 | GPSRST      | Reset         | 10| GND          | Ground       |
+---+-------------+---------------+---+--------------+--------------+
| 11| GPS_RFIN    | GPS signal    | 12| GND          | Ground       |
|   |             | input         |   |              |              |
+---+-------------+---------------+---+--------------+--------------+
| 13| NC          | Not connect   | 14| RFVCC        | Output       |
|   |             |               |   |              | Voltage RF   |
|   |             |               |   |              | section      |
+---+-------------+---------------+---+--------------+--------------+
| 15| NC          | Not connect   | 16| NC           | Not connect  |
+---+-------------+---------------+---+--------------+--------------+
| 17| NC          | Not connect   | 18| NC           | Not connect  |
+---+-------------+---------------+---+--------------+--------------+

2.13 WiFi&Bluetooth (U11)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. image:: image/21-wifi.gif
    :align: center
    
AP6236 is a low-power consumption module which has incorporated Wi-Fi
and Bluetooth into one chip. The module complies with IEEE 802.11 b/g/n
standard and it could achieve up to a speed of 72.2Mbps with single
stream in 802.11n draft, 54Mbps as specified in 802.11g, or 11Mbps for
802.11b to connect to the wireless LAN.

Features

-  802.11b/g/n single-band radio
-  Bluetooth V4.0(HS) with integrated Class 1.5 PA and Low Energy (BLE)
   support
-  Concurrent Bluetooth, WLAN operation
-  Simultaneous BT/WLAN receive with single antenna
-  WLAN host interface options:
- SDIO v2.0 — up to 50 MHz clock rate
-  BT host digital interface:
- UART (up to 4 Mbps)
-  IEEE Co-existence technologies are integrated die solution
-  ECI — enhanced coexistence support, ability to coordinate BT SCO
   transmissions around WLAN receives

+---+--------------+----------------+---+------------+---------------+
|Pin| Signal       | Description    |Pin| Signal     | Description   |
+---+--------------+----------------+---+------------+---------------+
| 1 | GND          | Ground         | 2 | WL_BT_ANT  | RF I/O        |
+---+--------------+----------------+---+------------+---------------+
| 3 | GND          | Ground         | 4 | NC         | Not connect   |
+---+--------------+----------------+---+------------+---------------+
| 5 | NC           | Not connect    | 6 | BT_WAKE    | HOST wake-up  |
|   |              |                |   |            | Bluetooth     |
|   |              |                |   |            | device        |
+---+--------------+----------------+---+------------+---------------+
| 7 | BT_HOST_WAKE | Bluetooth      | 8 | NC         | Not connect   |
|   |              | device to      |   |            |               |
|   |              | wake-up HOST   |   |            |               |
+---+--------------+----------------+---+------------+---------------+
| 9 | VBAT_WL      | Main power     | 10| XTAL_IN    | Crystal input |
|   |              | voltage source |   |            |               |
|   |              | input          |   |            |               |
+---+--------------+----------------+---+------------+---------------+
| 11| XTAL_OUT     | Crystal output | 12| W          | Internal      |
|   |              |                |   | IFI_REG_ON | regulators    |
|   |              |                |   |            | power enable  |
|   |              |                |   |            | / disable     |
+---+--------------+----------------+---+------------+---------------+
| 13| WI           | External       | 14| WIFI_D2    | WiFi data     |
|   | FI_HOST_WAKE | Interrupt      |   |            |               |
|   |              | Input / Keypad |   |            |               |
|   |              | input          |   |            |               |
+---+--------------+----------------+---+------------+---------------+
| 15| WIFI_D3      | WiFi data      | 16| WIFI_CMD   | WiFi command  |
+---+--------------+----------------+---+------------+---------------+
| 17| WIFI_CLK     | WiFi clock     | 18| WIFI_D0    | WiFi data     |
+---+--------------+----------------+---+------------+---------------+
| 19| WIFI_D1      | WiFi data      | 20| GND        | Ground        |
+---+--------------+----------------+---+------------+---------------+
| 21| VIN_LDO_OUT  | Internal Buck  | 22| VCCIO_WL   | I/O Voltage   |
|   |              | voltage        |   |            | supply input  |
|   |              | generation pin |   |            |               |
+---+--------------+----------------+---+------------+---------------+
| 23| VIN_LDO      | Internal Buck  | 24| LPO        | External Low  |
|   |              | voltage        |   |            | Power Clock   |
|   |              | generation pin |   |            | input         |
|   |              |                |   |            | (32.768KHz)   |
+---+--------------+----------------+---+------------+---------------+
| 25| NC           | Not connect    | 26| NC         | Not connect   |
+---+--------------+----------------+---+------------+---------------+
| 27| NC           | Not connect    | 28| NC         | Not connect   |
+---+--------------+----------------+---+------------+---------------+
| 29| NC           | Not connect    | 30| NC         | Not connect   |
+---+--------------+----------------+---+------------+---------------+
| 31| GND          | Ground         | 32| NC         | Not connect   |
+---+--------------+----------------+---+------------+---------------+
| 33| GND          | Ground         | 34| BT_RST     | Bluetooth     |
+---+--------------+----------------+---+------------+---------------+
| 35| NC           | Not connect    | 36| GND        | Ground        |
+---+--------------+----------------+---+------------+---------------+
| 37| NC           | Not connect    | 38| NC         | Not connect   |
+---+--------------+----------------+---+------------+---------------+
| 39| NC           | Not connect    | 40| NC         | Not connect   |
+---+--------------+----------------+---+------------+---------------+
| 41| UART0_CTS    | Bluetooth UART | 42| UART0_RX   | Bluetooth     |
|   |              | interface      |   |            | UART          |
|   |              |                |   |            | interface     |
+---+--------------+----------------+---+------------+---------------+
| 43| UART0_TX     | Bluetooth UART | 44| UART0_RTS  | Bluetooth     |
|   |              | interface      |   |            | UART          |
|   |              |                |   |            | interface     |
+---+--------------+----------------+---+------------+---------------+

2.14 Debug UART (J10)
^^^^^^^^^^^^^^^^^^^

.. image:: image/22-Debug.gif
    :align: center
    
The debug serial port (UART2) is used to connect PC and board with the
USB-to-serial cable (CP2102).

+---+-------------+---------------+---+--------------+--------------+
|Pin| Signal      | Description   |Pin| Signal       | Description  |
+---+-------------+---------------+---+--------------+--------------+
| 1 | UART2_RX    | UART2 receive | 2 | UART2_TX     | UART2        |
|   |             |               |   |              | transmit     |
+---+-------------+---------------+---+--------------+--------------+
| 3 | GND         | Ground        |                                 |
+---+-------------+---------------+---+--------------+--------------+

2.15 GPIO (CON4)
^^^^^^^^^^^^^^^^^^^

The GPIO is a 40-pin header connector. The pins can be defined as data
input/output.

.. image:: image/23-EM3288_GPIO.gif
    :align: center
    
+---+-------------+---------------+---+--------------+--------------+
| GPIO (CON4)                                                       |
+---+-------------+---------------+---+--------------+--------------+
|Pin| Signal      | Description   |Pin| Signal       | Description  |
+---+-------------+---------------+---+--------------+--------------+
| 1 | ADC2_IN     | ADC2 input    | 2 | ADC0_IN      | ADC0 input   |
+---+-------------+---------------+---+--------------+--------------+
| 3 | SPI0        | SPI0 clock/   | 4 | SPI0         | SPI0 Chip    |
|   | _CLK/TS0_D4 | TSI data4     |   | _CSn0/TS0_D5 | Select/ TSI  |
|   |             |               |   |              | data5        |
+---+-------------+---------------+---+--------------+--------------+
| 5 | SPI0_UART4  | UART4 receive | 6 | SPI0_UART    | UART4        |
|   | _RXD/TS0_D7 | data/ TSI     |   | 4_TXD/TS0_D6 | transmit     |
|   |             | data7         |   |              | data/ TSI    |
|   |             |               |   |              | data6        |
+---+-------------+---------------+---+--------------+--------------+
| 7 | UART1_C     | UART1 clear   | 8 | TS0_SYNC     | TSI          |
|   | TSn/TS0_D2  | to send/ TSI  |   |              | synchronizer |
|   |             | data2         |   |              | signal       |
+---+-------------+---------------+---+--------------+--------------+
| 9 | UART        | UART1         | 10| UART1        | UART1        |
|   | 1_RX/TS0_D0 | receive/ TSI  |   | _RTSn/TS0_D3 | ready-to-send|
|   |             | data0         |   |              | output/ TSI  |
|   |             |               |   |              | data3        |
+---+-------------+---------------+---+--------------+--------------+
| 11| TS0_CLK     | TSI reference | 12| UAR          | UART1        |
|   |             | clock         |   | T1_TX/TS0_D1 | transmit/    |
|   |             |               |   |              | TSI data1    |
+---+-------------+---------------+---+--------------+--------------+
| 13| TS0_ERR     | TSI fail      | 14| TS0_VALID    | TSI valid    |
|   |             | signal        |   |              | signal       |
+---+-------------+---------------+---+--------------+--------------+
| 15| I2C3_SCL    | I2C3 serial   | 16| I2C3_SDA     | I2C3 serial  |
|   |             | clock         |   |              | data         |
+---+-------------+---------------+---+--------------+--------------+
| 17| CIF_CLKOUT  | Camera0       | 18| CIF_CLKIN    | Camera0      |
|   |             | interface     |   |              | interface    |
|   |             | output work   |   |              | input pixel  |
|   |             | clock         |   |              | clock        |
+---+-------------+---------------+---+--------------+--------------+
| 19| CIF_HREF    | Camera0       | 20| CIF_VSYNC    | Camera0      |
|   |             | interface     |   |              | interface    |
|   |             | horizontal    |   |              | vertical     |
|   |             | sync signal   |   |              | sync signal  |
+---+-------------+---------------+---+--------------+--------------+
| 21| GPIO1_B7    | GPIO          | 22| GPIO1_B6     | GPIO         |
+---+-------------+---------------+---+--------------+--------------+
| 23| CIF_D9      | Camera0       | 24| CIF_D8       | Camera0      |
|   |             | interface     |   |              | interface    |
|   |             | input pixel   |   |              | input pixel  |
|   |             | data9         |   |              | data8        |
+---+-------------+---------------+---+--------------+--------------+
| 25| CIF_D7      | Camera0       | 26| CIF_D6       | Camera0      |
|   |             | interface     |   |              | interface    |
|   |             | input pixel   |   |              | input pixel  |
|   |             | data7         |   |              | data6        |
+---+-------------+---------------+---+--------------+--------------+
| 27| CIF_D5      | Camera0       | 28| CIF_D4       | Camera0      |
|   |             | interface     |   |              | interface    |
|   |             | input pixel   |   |              | input pixel  |
|   |             | data5         |   |              | data4        |
+---+-------------+---------------+---+--------------+--------------+
| 29| CIF_D3      | Camera0       | 30| CIF_D2       | Camera0      |
|   |             | interface     |   |              | interface    |
|   |             | input pixel   |   |              | input pixel  |
|   |             | data3         |   |              | data2        |
+---+-------------+---------------+---+--------------+--------------+
| 31| CIF_D1      | Camera0       | 32| CIF_D0       | Camera0      |
|   |             | interface     |   |              | interface    |
|   |             | input pixel   |   |              | input pixel  |
|   |             | data1         |   |              | data0        |
+---+-------------+---------------+---+--------------+--------------+
| 33| GND         | Ground        | 34| GND          | Ground       |
+---+-------------+---------------+---+--------------+--------------+
| 35| VCC_IO      | 3.3V          | 36| VCC_IO       | 3.3V         |
+---+-------------+---------------+---+--------------+--------------+
| 37| GND         | Ground        | 38| GND          | Ground       |
+---+-------------+---------------+---+--------------+--------------+
| 39| VCC5V       | 5V            | 40| VCC5V        | 5V           |
+---+-------------+---------------+---+--------------+--------------+

2.16 Control (J2)
^^^^^^^^^^^^^^^^^^^

The Pin6 of J2 is IR_IN. The EM3288 supports IR data receiver. The
signals are transmitted directly to the CPU.

.. image:: image/24-Control.gif   
  :align: center

+---+-------------+---------------+---+--------------+--------------+
|Pin| Signal      | Description   |Pin| Signal       | Description  |
+---+-------------+---------------+---+--------------+--------------+
| 1 | VCC_IO      | 3.3V          | 2 | GND          | Ground       |
+---+-------------+---------------+---+--------------+--------------+
| 3 | KEY_IN      | Recover key in| 4 | PWR_KEY      | Power key    |
+---+-------------+---------------+---+--------------+--------------+
| 5 | GND         | Ground        | 6 | IR_IN        | IR in        |
+---+-------------+---------------+---+--------------+--------------+
| 7 | WORK_LED    | Work LED      | 8 | PWR_LED      | Power LED    |
+---+-------------+---------------+---+--------------+--------------+

2.17 Buttons (K1, K2)
^^^^^^^^^^^^^^^^^^^^^^^^

.. image:: image/25-button.gif
   :align: center

Short press K1 is sleep/wake up and long press is reboot.

The K2 is used for download combined with OTG

+---+---------+-------------------+-----+------------+--------------+
|Key| Signal  | Description       | Key | Signal     | Description  |
+---+---------+-------------------+-----+------------+--------------+
| K1| PWR-KEY |Short: Sleep/WakeUp| K2  | RECOVER    | Download     |
|   |         |Long: Reboot       |     |            | mode         |
+---+---------+-------------------+-----+------------+--------------+

2.18 4G (CON2)
^^^^^^^^^^^^^^^^^^^

EM3288 adopts the standard PCI Express MiniCard form factor (MiniPCIe)
and provides global network coverage on the connectivity of LTE. It
delivers 50Mbps-up and100Mbps-down data rates on LTE FDD networks and
can also be fully backward compatible with existing UMTS and GSM/GPRS
networks.

**4G (EC20) Technical Specifications**

-  Form Factor: PCI Express Mini Card
-  Size: 51 x 30 x 4.9mm
-  Weight: 9.8g
-  Bandwidth: 1.4/3/5/10/15/20MHz
-  Temperature Range: -40°C ~ +80°C
-  Supply Voltage: 3.0V~3.6V, 3.3V Typical
-  3GPP TS27.007 and Enhanced AT Commands

.. image:: image/26-PCIe.gif

.. image:: image/27-4G.gif

+---+-----------+---+------------+---+------------+---+--------------+
| 4G Connector (CON2)                                                |
+---+-----------+---+------------+---+------------+---+--------------+
|Pin| Signal    |Pin| Signal     |Pin| Signal     |Pin| Signal       |
+---+-----------+---+------------+---+------------+---+--------------+
| 1 | NC        | 2 | 3GVCC      | 3 | NC         | 4 | GND          |
+---+-----------+---+------------+---+------------+---+--------------+
| 5 | NC        | 6 | NC         | 7 | NC         | 8 | SIM_VCC      |
+---+-----------+---+------------+---+------------+---+--------------+
| 9 | GND       | 10| SIM_DATA   | 11| NC         | 12| SIM_CLK      |
+---+-----------+---+------------+---+------------+---+--------------+
| 13| NC        | 14| SIM_RST    | 15| GND        | 16| NC           |
+---+-----------+---+------------+---+------------+---+--------------+
| 17| NC        | 18| GND        | 19| NC         | 20| 3GVCC        |
+---+-----------+---+------------+---+------------+---+--------------+
| 21| GND       | 22| 3G_PWEN    | 23| NC         | 24| 3GVCC        |
+---+-----------+---+------------+---+------------+---+--------------+
| 25| NC        | 26| GND        | 27| GND        | 28| NC           |
+---+-----------+---+------------+---+------------+---+--------------+
| 29| GND       | 30| NC         | 31| NC         | 32| NC           |
+---+-----------+---+------------+---+------------+---+--------------+
| 33| NC        | 34| GND        | 35| GND        | 36| USB_DM1      |
+---+-----------+---+------------+---+------------+---+--------------+
| 37| GND       | 38| USB_DP1    | 39| 3GVCC      | 40| GND          |
+---+-----------+---+------------+---+------------+---+--------------+
| 41| 3GVCC     | 42| LED_WWAN   | 43| GND        | 44| NC           |
+---+-----------+---+------------+---+------------+---+--------------+
| 45| NC        | 46| NC         | 47| NC         | 48| NC           |
+---+-----------+---+------------+---+------------+---+--------------+
| 49| NC        | 50| GND        | 51| NC         | 52| LED_RED. 3.3V|
+---+-----------+---+------------+---+------------+---+--------------+

.. image:: image/28-SIM.gif
   :align: center


P4 is an auto pop-up SIM card slot which is compatible to the standard
SIM Card and can be used for wireless transmission with a 3G/4G module.

+---+----------+-----------------+---+---------+---------------------+                                
| SIM Card slot (P4)                                                 |
+---+----------+-----------------+---+---------+---------------------+
|Pin| Signal   | Description     |Pin| Signal  | Description         |
+---+----------+-----------------+---+---------+---------------------+
| 1 | SIM_CLK  | Clock           | 2 | SIM_DATA| send/receive data   |
+---+----------+-----------------+---+---------+---------------------+
| 3 | SIM_RST  | Reset           | 4 | SIM_VCC | DC power supply     |
+---+----------+-----------------+---+---------+---------------------+
| 5 | SIM_VCC  | DC 5V power     | 6 | GND     | Ground              |
|   |          | supply          |   |         |                     |
+---+----------+-----------------+---+---------+---------------------+
| 7 | GND      | Ground          | 8 | GND     | Ground              |
+---+----------+-----------------+---+---------+---------------------+
| 9 | GND      | Ground          |                                   |
+---+----------+-----------------+---+---------+---------------------+

2.19 SATA & SATA_Power (J14, J18)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

On-board 7-pin SATA Interface, equipped with a HS USB to SATA bridge
JM20329. It requires 5V power supply. The SATA only supports mobile hard
disk, not desktop hard disk.

**Features**

-  Compliance with Gen1i/Gen1m of Serial ATA II Electrical Specification
   2.5

-  Support SATA II Asynchronous Signal Recovery (Hot Plug) feature

.. image:: image/29-SATA.gif
  :align: center

+---+-------------+---------------+---+--------------+--------------+
| SATA Connector (J14)                                              |
+---+-------------+---------------+---+--------------+--------------+
|Pin| Signal      | Description   |Pin| Signal       | Description  |
+---+-------------+---------------+---+--------------+--------------+
| 1 | GND         | Ground        | 2 | SATA_TXP     | Transmit +   |
+---+-------------+---------------+---+--------------+--------------+
| 3 | SATA_TXN    | Transmit -    | 4 | GND          | Ground       |
+---+-------------+---------------+---+--------------+--------------+
| 5 | SATA_RXN    | Receive -     | 6 | SATA_RXP     | Receive +    |
+---+-------------+---------------+---+--------------+--------------+
| 7 | GND         | Ground        |                                 |
+---+-------------+---------------+---+--------------+--------------+

.. image:: image/7-DC-SATA.gif
   :align: center

+---+-------------+---------------+---+--------------+--------------+
| SATA Power (J18)                                                  |
+---+-------------+---------------+---+--------------+--------------+
|Pin| Signal      | Description   |Pin| Signal       | Description  |
+---+-------------+---------------+---+--------------+--------------+
| 1 | SATA_5V     |SATA power.DC5V| 2 | GND          | Ground       |
+---+-------------+---------------+---+--------------+--------------+

2.20 RTC (BT1)
^^^^^^^^^^^^^^^^^^^

.. image:: image/31-RTC.gif
   :align: center

The backup battery (3V) is used to ensure the RTC (frequency 32.768KHz)
is still able to work after power off. Lithium cell model: CR1220.
