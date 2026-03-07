# ESPDuino-32
* Wemos D1 R32
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
# [설명서]< id="a">
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
* Arduino Uno Shield와 호환
* 6개의 ADC 채널
* 2개의 DAC 채널
* PWM 장치 2개, 총 7개 채널
* 1 x SPI 장치
* 1 x I2C 장치
* 2개의 UART 장치

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
![](img/3_Pinout_D1_R32.png)
* arduino_iomap.h
```
arduino_iomap.h
Go to the documentation of this file.
/*
 * SPDX-FileCopyrightText: 2025 Gunar Schorcht
 * SPDX-License-Identifier: LGPL-2.1-only
 */
 
#pragma once
 
#include "periph/gpio.h"
#include "periph/adc.h"
 
#ifdef __cplusplus
extern "C" {
#endif
 
#define ARDUINO_UART_D0D1       UART_DEV(0) 
#define ARDUINO_SPI_D11D12D13   SPI_DEV(0)  
#define ARDUINO_I2C_UNO         I2C_DEV(0)  
#define ARDUINO_LED             14          
#define ARDUINO_PIN_0   GPIO3       
#define ARDUINO_PIN_1   GPIO1       
 
#define ARDUINO_PIN_2   GPIO26
#define ARDUINO_PIN_3   GPIO25
#define ARDUINO_PIN_4   GPIO17
#define ARDUINO_PIN_5   GPIO16
#define ARDUINO_PIN_6   GPIO27
#define ARDUINO_PIN_7   GPIO14
#define ARDUINO_PIN_8   GPIO12
#define ARDUINO_PIN_9   GPIO13
 
#define ARDUINO_PIN_10  GPIO5
#define ARDUINO_PIN_11  GPIO23
#define ARDUINO_PIN_12  GPIO19
#define ARDUINO_PIN_13  GPIO18
 
/* analog pins as digital pin: */
#define ARDUINO_PIN_14  GPIO2       
#define ARDUINO_PIN_15  GPIO4       
#define ARDUINO_PIN_16  GPIO35      
#define ARDUINO_PIN_17  GPIO34      
#define ARDUINO_PIN_18  GPIO36      
#define ARDUINO_PIN_19  GPIO39      
 
/* I2C pins as digital pins */
#define ARDUINO_PIN_20  GPIO21      
#define ARDUINO_PIN_21  GPIO22      
 
#define ARDUINO_PIN_LAST    21      
#define ARDUINO_PIN_A0      ARDUINO_PIN_14   // GPIO2
#define ARDUINO_PIN_A1      ARDUINO_PIN_15   // GPIO4
#define ARDUINO_PIN_A2      ARDUINO_PIN_16   // GPIO35
#define ARDUINO_PIN_A3      ARDUINO_PIN_17   // GPIO34
#define ARDUINO_PIN_A4      ARDUINO_PIN_18   // GPIO36 
#define ARDUINO_PIN_A5      ARDUINO_PIN_19   // GPIO39
 
#define ARDUINO_PIN_DAC0    ARDUINO_PIN_3    
#define ARDUINO_PIN_DAC1    ARDUINO_PIN_2    
#define ARDUINO_A0          ADC_LINE(0)     
#define ARDUINO_A1          ADC_LINE(1)     
#define ARDUINO_A2          ADC_LINE(2)     
#define ARDUINO_A3          ADC_LINE(3)     
#define ARDUINO_A4          ADC_LINE(4)     
#define ARDUINO_A5          ADC_LINE(5)     
 
#define ARDUINO_ANALOG_PIN_LAST 5           
#define ARDUINO_DAC0        DAC_LINE(0)     
#define ARDUINO_DAC1        DAC_LINE(1)     
 
#define ARDUINO_DAC_PIN_LAST    1           
#define ARDUINO_PIN_3_PWM_DEV   PWM_DEV(0)  
#define ARDUINO_PIN_3_PWM_CHAN  0           
 
#define ARDUINO_PIN_5_PWM_DEV   PWM_DEV(0)  
#define ARDUINO_PIN_5_PWM_CHAN  1           
 
#define ARDUINO_PIN_6_PWM_DEV   PWM_DEV(0)  
#define ARDUINO_PIN_6_PWM_CHAN  2           
 
#define ARDUINO_PIN_9_PWM_DEV   PWM_DEV(0)  
#define ARDUINO_PIN_9_PWM_CHAN  3           
 
#define ARDUINO_PIN_10_PWM_DEV  PWM_DEV(1)  
#define ARDUINO_PIN_10_PWM_CHAN 0           
 
#define ARDUINO_PIN_11_PWM_DEV  PWM_DEV(1)  
#define ARDUINO_PIN_11_PWM_CHAN 1           
 
#ifdef __cplusplus
}
#endif

```


```
Definition in file arduino_iomap.h.

#include "periph/gpio.h"
#include "periph/adc.h"
Go to the source code of this file.

#define 	ARDUINO_UART_D0D1   UART_DEV(0)		// Arduino UART interface.
#define 	ARDUINO_SPI_D11D12D13   SPI_DEV(0)	// Arduino SPI bus.
#define 	ARDUINO_I2C_UNO   I2C_DEV(0)		// Arduino I2C bus.
#define 	ARDUINO_LED   14					// LED is connected to Arduino pin 14.

Mapping of MCU pins to Arduino pins
#define 	ARDUINO_PIN_0   GPIO3				// Arduino pin 0 (RxD)
#define 	ARDUINO_PIN_1   GPIO1				// Arduino pin 1 (TxD)
#define 	ARDUINO_PIN_2   GPIO26				// Arduino pin 2 (DAC1)
#define 	ARDUINO_PIN_3   GPIO25				// Arduino pin 3 (PWM / DAC0)
#define 	ARDUINO_PIN_4   GPIO17				// Arduino pin 4.
#define 	ARDUINO_PIN_5   GPIO16				// Arduino pin 5 (PWM)
#define 	ARDUINO_PIN_6   GPIO27				// Arduino pin 6 (PWM)
#define 	ARDUINO_PIN_7   GPIO14				// Arduino pin 7
#define 	ARDUINO_PIN_8   GPIO12				// Arduino pin 8
#define 	ARDUINO_PIN_9   GPIO13				// Arduino pin 9 (PWM)
#define 	ARDUINO_PIN_10   GPIO5
 	Arduino pin 10 (CS0 / PWM)
 
#define 	ARDUINO_PIN_11   GPIO23
 	Arduino pin 11 (MOSI / PWM)
 
#define 	ARDUINO_PIN_12   GPIO19
 	Arduino pin 12 (MISO)
 
#define 	ARDUINO_PIN_13   GPIO18
 	Arduino pin 13 (SCK)
 
#define 	ARDUINO_PIN_14   GPIO2
 	Arduino pin 14 (A0 / LED)
 
#define 	ARDUINO_PIN_15   GPIO4
 	Arduino pin 15 (A1)
 
#define 	ARDUINO_PIN_16   GPIO35
 	Arduino pin 16 (A2), input only!
 
#define 	ARDUINO_PIN_17   GPIO34
 	Arduino pin 17 (A3), input only!
 
#define 	ARDUINO_PIN_18   GPIO36
 	Arduino pin 18 (A4), input only!
 
#define 	ARDUINO_PIN_19   GPIO39
 	Arduino pin 19 (A5), input only!
 
#define 	ARDUINO_PIN_20   GPIO21
 	Arduino pin 20 (SDA)
 
#define 	ARDUINO_PIN_21   GPIO22
 	Arduino pin 21 (SCL)
 
#define 	ARDUINO_PIN_LAST   21
 	Last Arduino pin index.
 
Aliases for analog pins
#define 	ARDUINO_PIN_A0   ARDUINO_PIN_14
 	Arduino pin A0.
 
#define 	ARDUINO_PIN_A1   ARDUINO_PIN_15
 	Arduino pin A1.
 
#define 	ARDUINO_PIN_A2   ARDUINO_PIN_16
 	Arduino pin A2.
 
#define 	ARDUINO_PIN_A3   ARDUINO_PIN_17
 	Arduino pin A3.
 
#define 	ARDUINO_PIN_A4   ARDUINO_PIN_18
 	Arduino pin A4.
 
#define 	ARDUINO_PIN_A5   ARDUINO_PIN_19
 	Arduino pin A5.
 
#define 	ARDUINO_PIN_DAC0   ARDUINO_PIN_3
 	Arduino pin D3.
 
#define 	ARDUINO_PIN_DAC1   ARDUINO_PIN_2		// Arduino pin D2.

Mapping of Arduino analog pins to RIOT ADC lines
#define 	ARDUINO_A0   ADC_LINE(0)				// ADC line for Arduino pin A0.
#define 	ARDUINO_A1   ADC_LINE(1)				// ADC line for Arduino pin A1.
#define 	ARDUINO_A2   ADC_LINE(2)				// ADC line for Arduino pin A2.
#define 	ARDUINO_A3   ADC_LINE(3)				// ADC line for Arduino pin A3.
#define 	ARDUINO_A4   ADC_LINE(4)				// ADC line for Arduino pin A4.
#define 	ARDUINO_A5   ADC_LINE(5)				// ADC line for Arduino pin A5.
#define 	ARDUINO_ANALOG_PIN_LAST   5				// Last Arduino analog pin index.
 
Mapping of Arduino DAC pins to RIOT DAC lines
#define 	ARDUINO_DAC0   DAC_LINE(0)				// DAC line for Arduino DAC0 pin.
#define 	ARDUINO_DAC1   DAC_LINE(1)				// DAC line for Arduino DAC1 pin.
#define 	ARDUINO_DAC_PIN_LAST   1				// Last Arduino DAC pin index.

Mapping of Arduino pins to RIOT PWM dev and channel pairs
#define 	ARDUINO_PIN_3_PWM_DEV   PWM_DEV(0)		// PWM device for Arduino pin 3.
#define 	ARDUINO_PIN_3_PWM_CHAN   0				// PWM channel for Arduino pin 3.
#define 	ARDUINO_PIN_5_PWM_DEV   PWM_DEV(0)		// PWM device for Arduino pin 5.
#define 	ARDUINO_PIN_5_PWM_CHAN   1				// PWM channel for Arduino pin 5.
#define 	ARDUINO_PIN_6_PWM_DEV   PWM_DEV(0)		// PWM device for Arduino pin 6.
#define 	ARDUINO_PIN_6_PWM_CHAN   2				// PWM channel for Arduino pin 6.
#define 	ARDUINO_PIN_9_PWM_DEV   PWM_DEV(0)		// PWM device for Arduino pin 9.
#define 	ARDUINO_PIN_9_PWM_CHAN   3				// PWM channel for Arduino pin 9.
#define 	ARDUINO_PIN_10_PWM_DEV   PWM_DEV(1)		// PWM device for Arduino pin 10.
#define 	ARDUINO_PIN_10_PWM_CHAN   0				// PWM channel for Arduino pin 10.
#define 	ARDUINO_PIN_11_PWM_DEV   PWM_DEV(1)		// PWM device for Arduino pin 11.
#define 	ARDUINO_PIN_11_PWM_CHAN   1				// PWM channel for Arduino pin 11.
 
Macro Definition Documentation
#define ARDUINO_A0   ADC_LINE(0)					// ADC line for Arduino pin A0.

Definition at line 85 of file arduino_iomap.h.

#define ARDUINO_A1   ADC_LINE(1)
ADC line for Arduino pin A1.

Definition at line 86 of file arduino_iomap.h.

#define ARDUINO_A2   ADC_LINE(2)
ADC line for Arduino pin A2.

Definition at line 87 of file arduino_iomap.h.

#define ARDUINO_A3   ADC_LINE(3)
ADC line for Arduino pin A3.

Definition at line 88 of file arduino_iomap.h.

#define ARDUINO_A4   ADC_LINE(4)
ADC line for Arduino pin A4.

Definition at line 89 of file arduino_iomap.h.

#define ARDUINO_A5   ADC_LINE(5)
ADC line for Arduino pin A5.

Definition at line 90 of file arduino_iomap.h.

#define ARDUINO_ANALOG_PIN_LAST   5
Last Arduino analog pin index.

Definition at line 92 of file arduino_iomap.h.

#define ARDUINO_DAC0   DAC_LINE(0)
DAC line for Arduino DAC0 pin.

Definition at line 99 of file arduino_iomap.h.

#define ARDUINO_DAC1   DAC_LINE(1)
DAC line for Arduino DAC1 pin.

Definition at line 100 of file arduino_iomap.h.

#define ARDUINO_DAC_PIN_LAST   1
Last Arduino DAC pin index.

Definition at line 102 of file arduino_iomap.h.

#define ARDUINO_I2C_UNO   I2C_DEV(0)
Arduino I2C bus.

Definition at line 27 of file arduino_iomap.h.

#define ARDUINO_LED   14
LED is connected to Arduino pin 14.

Definition at line 28 of file arduino_iomap.h.

#define ARDUINO_PIN_0   GPIO3
Arduino pin 0 (RxD)

Definition at line 34 of file arduino_iomap.h.

#define ARDUINO_PIN_1   GPIO1
Arduino pin 1 (TxD)

Definition at line 35 of file arduino_iomap.h.

#define ARDUINO_PIN_10   GPIO5
Arduino pin 10 (CS0 / PWM)

Definition at line 46 of file arduino_iomap.h.

#define ARDUINO_PIN_10_PWM_CHAN   0
PWM channel for Arduino pin 10.

Definition at line 122 of file arduino_iomap.h.

#define ARDUINO_PIN_10_PWM_DEV   PWM_DEV(1)
PWM device for Arduino pin 10.

Definition at line 121 of file arduino_iomap.h.

#define ARDUINO_PIN_11   GPIO23
Arduino pin 11 (MOSI / PWM)

Definition at line 47 of file arduino_iomap.h.

#define ARDUINO_PIN_11_PWM_CHAN   1
PWM channel for Arduino pin 11.

Definition at line 125 of file arduino_iomap.h.

#define ARDUINO_PIN_11_PWM_DEV   PWM_DEV(1)
PWM device for Arduino pin 11.

Definition at line 124 of file arduino_iomap.h.

#define ARDUINO_PIN_12   GPIO19
Arduino pin 12 (MISO)

Definition at line 48 of file arduino_iomap.h.

#define ARDUINO_PIN_13   GPIO18
Arduino pin 13 (SCK)

Definition at line 49 of file arduino_iomap.h.

#define ARDUINO_PIN_14   GPIO2
Arduino pin 14 (A0 / LED)

Definition at line 52 of file arduino_iomap.h.

#define ARDUINO_PIN_15   GPIO4
Arduino pin 15 (A1)

Definition at line 53 of file arduino_iomap.h.

#define ARDUINO_PIN_16   GPIO35
Arduino pin 16 (A2), input only!

Definition at line 54 of file arduino_iomap.h.

#define ARDUINO_PIN_17   GPIO34
Arduino pin 17 (A3), input only!

Definition at line 55 of file arduino_iomap.h.

#define ARDUINO_PIN_18   GPIO36
Arduino pin 18 (A4), input only!

Definition at line 56 of file arduino_iomap.h.

#define ARDUINO_PIN_19   GPIO39
Arduino pin 19 (A5), input only!

Definition at line 57 of file arduino_iomap.h.

#define ARDUINO_PIN_2   GPIO26
Arduino pin 2 (DAC1)

Definition at line 37 of file arduino_iomap.h.

#define ARDUINO_PIN_20   GPIO21
Arduino pin 20 (SDA)

Definition at line 60 of file arduino_iomap.h.

#define ARDUINO_PIN_21   GPIO22
Arduino pin 21 (SCL)

Definition at line 61 of file arduino_iomap.h.

#define ARDUINO_PIN_3   GPIO25
Arduino pin 3 (PWM / DAC0)

Definition at line 38 of file arduino_iomap.h.

#define ARDUINO_PIN_3_PWM_CHAN   0
PWM channel for Arduino pin 3.

Definition at line 110 of file arduino_iomap.h.

#define ARDUINO_PIN_3_PWM_DEV   PWM_DEV(0)
PWM device for Arduino pin 3.

Definition at line 109 of file arduino_iomap.h.

#define ARDUINO_PIN_4   GPIO17
Arduino pin 4.

Definition at line 39 of file arduino_iomap.h.

#define ARDUINO_PIN_5   GPIO16
Arduino pin 5 (PWM)

Definition at line 40 of file arduino_iomap.h.

#define ARDUINO_PIN_5_PWM_CHAN   1
PWM channel for Arduino pin 5.

Definition at line 113 of file arduino_iomap.h.

#define ARDUINO_PIN_5_PWM_DEV   PWM_DEV(0)
PWM device for Arduino pin 5.

Definition at line 112 of file arduino_iomap.h.

#define ARDUINO_PIN_6   GPIO27
Arduino pin 6 (PWM)

Definition at line 41 of file arduino_iomap.h.

#define ARDUINO_PIN_6_PWM_CHAN   2
PWM channel for Arduino pin 6.

Definition at line 116 of file arduino_iomap.h.

#define ARDUINO_PIN_6_PWM_DEV   PWM_DEV(0)
PWM device for Arduino pin 6.

Definition at line 115 of file arduino_iomap.h.

#define ARDUINO_PIN_7   GPIO14
Arduino pin 7.

Definition at line 42 of file arduino_iomap.h.

#define ARDUINO_PIN_8   GPIO12
Arduino pin 8.

Definition at line 43 of file arduino_iomap.h.

#define ARDUINO_PIN_9   GPIO13
Arduino pin 9 (PWM)

Definition at line 44 of file arduino_iomap.h.

#define ARDUINO_PIN_9_PWM_CHAN   3
PWM channel for Arduino pin 9.

Definition at line 119 of file arduino_iomap.h.

#define ARDUINO_PIN_9_PWM_DEV   PWM_DEV(0)
PWM device for Arduino pin 9.

Definition at line 118 of file arduino_iomap.h.

#define ARDUINO_PIN_A0   ARDUINO_PIN_14
Arduino pin A0.

Definition at line 70 of file arduino_iomap.h.

#define ARDUINO_PIN_A1   ARDUINO_PIN_15
Arduino pin A1.

Definition at line 71 of file arduino_iomap.h.

#define ARDUINO_PIN_A2   ARDUINO_PIN_16
Arduino pin A2.

Definition at line 72 of file arduino_iomap.h.

#define ARDUINO_PIN_A3   ARDUINO_PIN_17
Arduino pin A3.

Definition at line 73 of file arduino_iomap.h.

#define ARDUINO_PIN_A4   ARDUINO_PIN_18
Arduino pin A4.

Definition at line 74 of file arduino_iomap.h.

#define ARDUINO_PIN_A5   ARDUINO_PIN_19
Arduino pin A5.

Definition at line 75 of file arduino_iomap.h.

#define ARDUINO_PIN_DAC0   ARDUINO_PIN_3
Arduino pin D3.

Definition at line 77 of file arduino_iomap.h.

#define ARDUINO_PIN_DAC1   ARDUINO_PIN_2
Arduino pin D2.

Definition at line 78 of file arduino_iomap.h.

#define ARDUINO_PIN_LAST   21
Last Arduino pin index.

Definition at line 63 of file arduino_iomap.h.

#define ARDUINO_SPI_D11D12D13   SPI_DEV(0)
Arduino SPI bus.

Definition at line 26 of file arduino_iomap.h.

#define ARDUINO_UART_D0D1   UART_DEV(0)
Arduino UART interface.

Definition at line 25 of file arduino_iomap.h.


```
# [추가예정]