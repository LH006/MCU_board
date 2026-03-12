# ESP32

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

***
# [종류]
* ESP32-WROOM-32 module
* 
*
![](img/2.png)

# [회로도]
![보드](img/WenosD1R32_.jpg)
![](img/1.png)
***

---

# ESP32-S(또는 ESP32-WROOM-32S)
* 통신: 2.4GHz Wi-Fi (802.11 b/g/n)
* Bluetooth 4.2/LE
* 프로세서: Xtensa 듀얼 코어 32비트 LX6
* 최대 240MHz 동작
* 메모리: 일반적으로 4MB SPI 플래시 내장
* 통합 저전력 SoC로 낮은 전력 소비
* 풍부한 페리페럴(ADC, DAC, I2C, SPI, UART 등)
---



# [보드 구성]
* Arduino Uno Shield와 호환
* 6개의 ADC 채널
* 2개의 DAC 채널
* PWM 장치 2개, 총 7개 채널
* 1 x SPI 장치
* 1 x I2C 장치
* 2개의 UART 장치

# [라이브러리]
* 

* 웹 소켓 사용
***
# [즐겨찾기]
* https://github.com/espressif/arduino-esp32
* https://cafe.naver.com/lsg20004/873
* https://cafe.naver.com/lh0006/2292
***

# [핀 배열]
![](img/3_Pinout_D1_R32.png)
* Pin 사용법 예제(https://docs.espressif.com/projects/arduino-esp32/en/latest/libraries.html)

### 모두 핀
```
* Analog inputs 12bit(0~3V)
* Analog outputs 8bit(0~3V)
* GPIO 0    //ADC2_CH1  //터치1 //RTC11 //PWM가능 //인터럽트 가능
* GPIO 1    //U0-TX //인터럽트 가능
* GPIO 2    //ADC2_CH2  //터치2 //RTC12 //PWM가능 //내부풀업 안됨 //인터럽트 가능
* GPIO 3    //U0-RX //인터럽트 가능
* GPIO 4    //ADC2_CH0  //터치0 //RTC10 //PWM가능 //내부풀업 가능 //인터럽트 가능
* GPIO 5    //SPI-SS    //내부풀업 가능 //인터럽트 가능
* GPIO 6    //인터럽트 불가
* GPIO 7    //인터럽트 불가
* GPIO 8    //인터럽트 불가
* GPIO 9    //인터럽트 불가
* GPIO 10   //내부풀업 가능 //인터럽트 불가
* GPIO 11   //내부풀업 가능 //인터럽트 불가
* GPIO 12   //ADC2_CH5  //터치5 //RTC15 //SD-D2 //HSPI bus-Q //내부풀업 가능 //인터럽트 가능
* GPIO 13   //ADC2_CH4  //터치4 //RTC14 //SD-D3 //HSPI bus-D //내부풀업 가능 //인터럽트 가능
* GPIO 14   //ADC2_CH6  //터치6 //RTC16 //SD-CLK //HSPI bus-CL //내부풀업 가능 //인터럽트 가능
* GPIO 15   //ADC2_CH3  //터치3 //RTC13 //SDCMD //HSPI bus-C5 //내부풀업 가능  //인터럽트 가능
* GPIO 16   //U2-RX //인터럽트 가능
* GPIO 17   //U2-TX //인터럽트 가능
* GPIO 18   //SPI-SCK   //인터럽트 가능
* GPIO 19   //SPI-MISO  //인터럽트 가능
* GPIO 20
* GPIO 21   //SDA   //인터럽트 가능
* GPIO 22   //SCL   //인터럽트 가능
* GPIO 23   //SPI-MOSI  //내부풀업 안됨     //인터럽트 가능
* GPIO 24
* GPIO 25   //ADC2_CH8  //RTC6  //DAC1(OUT 8BIT 0~3V)    //인터럽트 가능
* GPIO 26   //ADC2_CH9  //RTC7  //DAC2(OUT 8BIT 0~3V)    //내부풀업 안됨 //인터럽트 가능
* GPIO 27   //ADC2_CH7  //터치7 //RTC17 //인터럽트 가능
* GPIO 28
* GPIO 29
* GPIO 30
* GPIO 31
* GPIO 32   //ADC1_CH4  //터치9  //RTC9    //내부풀업 안됨     //인터럽트 가능
* GPIO 33   //ADC1_CH5  //터치8  //RTC8    //내부풀업 가능     //인터럽트 가능
* GPIO 34   //ADC1_CH6  //RTC4  //입력전용  //내부풀업 안됨     //인터럽트 가능
* GPIO 35   //입력전용  //내부풀업 안됨     //인터럽트 가능
* GPIO 36   //ADC1_CH7  //RTC5  //입력전용  //내부풀업 안됨   //인터럽트 가능
* GPIO 37   //ADC1_CH1  //입력전용  //내부풀업 안됨     
* GPIO 38   //입력전용  //내부풀업 안됨
* GPIO 39   //ADC1_CH3  //RTC3  //입력전용  //내부풀업 안됨     //인터럽트 가능
```

### [# 내부 터치 센서]
* T0 (GPIO 4)
* T1 (GPIO 0)
* T2 (GPIO 2)
* T3 (GPIO 15)
* T4 (GPIO 13)
* T5 (GPIO 12)
* T6 (GPIO 14)
* T7 (GPIO 27)
* T8 (GPIO 33)
* T9 (GPIO 32)

### [# SPI] ESP-WROOM-32
* GPIO 6 (SCK/CLK)
* GPIO 7 (SDO/SD0)
* GPIO 8 (SDI/SD1)
* GPIO 9 (SHD/SD2)
* GPIO 10 (SWP/SD3)
* GPIO 11 (CSC/CMD)

### [# I2C]
* GPIO 21 (SDA)
* GPIO 22 (SCL)
```
/* I2C pins as digital pins */
#define ARDUINO_PIN_20  GPIO21      // (SDA)
#define ARDUINO_PIN_21  GPIO22      // (SCL)

```
### GPIO 34~39는 PWM을 만들 수 없음
* GPIO 34 //입력전용 //내부풀업 안됨
* GPIO 35 //입력전용 //내부풀업 안됨
* GPIO 36 //입력전용 //내부풀업 안됨
* GPIO 37 //입력전용 //내부풀업 안됨
* GPIO 38 //입력전용 //내부풀업 안됨
* GPIO 39 //입력전용 //내부풀업 안됨

### [# ADC] (
* Analog-to-Digital Converter
* ESP32는 18개의 12-bit ADC 채널
* (ESP8266의 경우는 1개의 10-bit ADC만 가지고 있음)

 * ADC1_CH0 (GPIO 36)
 * ADC1_CH1 (GPIO 37)
 * ADC1_CH2 (GPIO 38)
 * ADC1_CH3 (GPIO 39)
 * ADC1_CH4 (GPIO 32)
 * ADC1_CH5 (GPIO 33)
 * ADC1_CH6 (GPIO 34)
 * ADC1_CH7 (GPIO 35)
 * ADC2_CH0 (GPIO 4)
 * ADC2_CH1 (GPIO 0)
 * ADC2_CH2 (GPIO 2)
 * ADC2_CH3 (GPIO 15)
 * ADC2_CH4 (GPIO 13)
 * ADC2_CH5 (GPIO 12)
 * ADC2_CH6 (GPIO 14)
 * ADC2_CH7 (GPIO 27)
 * ADC2_CH8 (GPIO 25)
 * ADC2_CH9 (GPIO 26)
```
정리중
/* analog pins as digital pin: */
#define ARDUINO_PIN_14  GPIO2       
#define ARDUINO_PIN_15  GPIO4       
#define ARDUINO_PIN_16  GPIO35      
#define ARDUINO_PIN_17  GPIO34      
#define ARDUINO_PIN_18  GPIO36      
#define ARDUINO_PIN_19  GPIO39      

#define ARDUINO_PIN_A0      ARDUINO_PIN_14   // GPIO2
#define ARDUINO_PIN_A1      ARDUINO_PIN_15   // GPIO4
#define ARDUINO_PIN_A2      ARDUINO_PIN_16   // GPIO35
#define ARDUINO_PIN_A3      ARDUINO_PIN_17   // GPIO34
#define ARDUINO_PIN_A4      ARDUINO_PIN_18   // GPIO36 
#define ARDUINO_PIN_A5      ARDUINO_PIN_19   // GPIO39


```

### RTC GPIO
ESP32는 RTC GPIO를 지원한다. ESP32가 deep sleep 모드에 있을 때 RTC의 low-power subsystem에 연결된 GPIO를 사용할 수 있다. 이 RTC GPIO는 ULP(Ultra Low Power) 코프로세서가 실행중일 때 ESP32를 deep sleep에서 깨어나게 하는데 사용된다. 다음의 GPIO들이 외부 wake up 소스로 사용될 수 있다.
* RTC_GPIO0 (GPIO 36)
* RTC_GPIO3 (GPIO 39)
* RTC_GPIO4 (GPIO 34)
* RTC_GPIO5 (GPIO 35)
* RTC_GPIO6 (GPIO 25)
* RTC_GPIO7 (GPIO 26)
* RTC_GPIO8 (GPIO 33)
* RTC_GPIO9 (GPIO 32)
* RTC_GPIO10 (GPIO 4)
* RTC_GPIO11 (GPIO 0)
* RTC_GPIO12 (GPIO 2)
* RTC_GPIO13 (GPIO 15)
* RTC_GPIO14 (GPIO 13)
* RTC_GPIO15 (GPIO 12)
* RTC_GPIO16 (GPIO 14)
* RTC_GPIO17 (GPIO 27)

### DAC (Digital-to-Analog Converter)
ESP32에는 2개의 8-bit DAC 채널이 있어 디지털 신호를 아날로그 전압으로 바꿔 출력해 준다.
* DAC1 (GPIO 25)
* DAC2 (GPIO 26)
***


```
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

// Mapping of MCU pins to Arduino pins
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
#define 	ARDUINO_PIN_10  GPIO5               // Arduino pin 10 (CS0 / PWM)
#define 	ARDUINO_PIN_11  GPIO23              // Arduino pin 11 (MOSI / PWM)
#define 	ARDUINO_PIN_12  GPIO19              // Arduino pin 12 (MISO)
#define 	ARDUINO_PIN_13  GPIO18              // Arduino pin 13 (SCK)
#define 	ARDUINO_PIN_14  GPIO2               // Arduino pin 14 (A0 / LED)
#define 	ARDUINO_PIN_15  GPIO4               // Arduino pin 15 (A1)
#define 	ARDUINO_PIN_16  GPIO35				// Arduino pin 16 (A2), input only!
 
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

// Mapping of Arduino analog pins to RIOT ADC lines
#define 	ARDUINO_A0   ADC_LINE(0)				// ADC line for Arduino pin A0.
#define 	ARDUINO_A1   ADC_LINE(1)				// ADC line for Arduino pin A1.
#define 	ARDUINO_A2   ADC_LINE(2)				// ADC line for Arduino pin A2.
#define 	ARDUINO_A3   ADC_LINE(3)				// ADC line for Arduino pin A3.
#define 	ARDUINO_A4   ADC_LINE(4)				// ADC line for Arduino pin A4.
#define 	ARDUINO_A5   ADC_LINE(5)				// ADC line for Arduino pin A5.
#define 	ARDUINO_ANALOG_PIN_LAST   5				// Last Arduino analog pin index.
 
// Mapping of Arduino DAC pins to RIOT DAC lines
#define 	ARDUINO_DAC0   DAC_LINE(0)				// DAC line for Arduino DAC0 pin.
#define 	ARDUINO_DAC1   DAC_LINE(1)				// DAC line for Arduino DAC1 pin.
#define 	ARDUINO_DAC_PIN_LAST   1				// Last Arduino DAC pin index.

// Mapping of Arduino pins to RIOT PWM dev and channel pairs
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
 
// Macro Definition Documentation
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

* 파일
```
#ifndef Pins_Arduino_h
#define Pins_Arduino_h

#include <stdint.h>

static const uint8_t TX = 1;
static const uint8_t RX = 3;

static const uint8_t SDA = 21;
static const uint8_t SCL = 22;

static const uint8_t SS = 5;
static const uint8_t MOSI = 23;
static const uint8_t MISO = 19;
static const uint8_t SCK = 18;

static const uint8_t A0 = 36;
static const uint8_t A3 = 39;
static const uint8_t A4 = 32;
static const uint8_t A5 = 33;
static const uint8_t A6 = 34;
static const uint8_t A7 = 35;
static const uint8_t A10 = 4;
static const uint8_t A11 = 0;
static const uint8_t A12 = 2;
static const uint8_t A13 = 15;
static const uint8_t A14 = 13;
static const uint8_t A15 = 12;
static const uint8_t A16 = 14;
static const uint8_t A17 = 27;
static const uint8_t A18 = 25;
static const uint8_t A19 = 26;

static const uint8_t T0 = 4;
static const uint8_t T1 = 0;
static const uint8_t T2 = 2;
static const uint8_t T3 = 15;
static const uint8_t T4 = 13;
static const uint8_t T5 = 12;
static const uint8_t T6 = 14;
static const uint8_t T7 = 27;
static const uint8_t T8 = 33;
static const uint8_t T9 = 32;

static const uint8_t DAC1 = 25;
static const uint8_t DAC2 = 26;

#endif /* Pins_Arduino_h */
```
# [추가예정]