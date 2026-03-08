# LOLIN D32 (ESP32)
*
* 
***
# [목록]
* [설명서](#설명서)
* [보드](#보드)
* [회로도](#회로도)
* [보드 구성](#보드-구성)
* [라이브러리](#추가-라이브러리)
* [즐겨찾기](#즐겨찾기)
* [핀 배열](#핀-배열)
* [추가예정](#추가예정)

***
# [설명서]
* [ESP32 내용](https://github.com/LH006/MCU_board/tree/main/ESP32)
*

***
# [보드]
![](img/2.png)

# [회로도]
![보드](img/WenosD1R32_.jpg)
![](img/1.png)
***
# [보드 구성]
* ESP32-WROOM-32 module
* Flash Memory: 4 MB (some versions have 16 MB)
* SRAM: 520 KB
* Connectivity:
   * Wi-Fi 802.11 b/g/n
   * Bluetooth v4.2 BR/EDR and BLE
* Operating Voltage: 3.3 V logic
* USB-to-Serial: CP2104 or CH340C (depends on version)
   * Power Supply:
   * USB 5 V
   * LiPo battery (with built-in charger)
* Battery Charging: Integrated Li-ion/LiPo charger (via JST-PH connector)
* GPIO Pins: 34 (some reserved for internal functions)
* Analog Inputs: 12-bit ADC (up to 18 channels)
* DAC Outputs: 2 channels (8-bit)
* PWM: Up to 16 channels
* I²C, SPI, UART: Multiple hardware interfaces

# [라이브러리]
* [WiFiManager](https://github.com/tzapu/WiFiManager)
* Wifi
* [WebSocketSerialMonitor](https://github.com/tzapu/WebSocketSerialMonitor)
* 웹 소켓 사용
***
# [즐겨찾기]
* https://cafe.naver.com/lsg20004/873
* https://cafe.naver.com/lh0006/2292
***

# [핀 배열]
![](img/.png)
* arduino_iomap.h
```
// 보드
// 좌쪽
// X // GPIO36 //ADC1_CH0 // 센서VP //입력전용
// X // GPIO39 //ADC1_CH3 // 센서VN //입력전용
// X // GPIO34 //ADC1_CH6 //입력전용
// R4 // GPIO32 //ADC1_CH4
// R5 // GPIO33 //ADC1_CH5
// R6 // GPIO25 //ADC2_CH8 //DAC1
// R7 // GPIO26 //ADC2_CH9 //DAC2
// R8 // GPIO27 //ADC2_CH7
// R1 // GPIO14 //ADC2_CH6
// R2 // GPIO12 //ADC2_CH5
// R3 // GPIO13 //ADC2_CH4

// 우쪽
//  L1 //GPIO23 //L1
//  L2 //GPIO22 //L2
//  X //GPIO1 // TXD0
//  X //GPIO3 // RXD0
//  L3 //GPIO21 //L3
//  L4 //GPIO19 //L4
//  X //GPIO18
// 내장LED //GPIO5
//  X //GPIO17 //TXD2
//  X //GPIO16 //RXD2
//  X //GPIO4 //ADC2_CH0
//  X //GPIO0 //ADC2_CH1
//  X //GPIO2 //ADC2_CH2
//  X //GPIO15 //ADC2_CH3

```
# [추가예정]
