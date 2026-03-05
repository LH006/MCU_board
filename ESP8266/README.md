9# WEB 스위치 On/OFF 제어
***
# [목록]
* [설명서](#설명서)
* [추가예정](#추가예정)
* [보드정보](#보드-ESP8266)
* [라이브러리](#추가-라이브러리)
* [즐겨찾기](#즐겨찾기)
***
# [설명서]
* (1)
*
# [추가예정]
* (1) 웹 시리얼 만들기 포트:81
***
# [보드 ESP8266]
![](/img/IMG_5590.png)
![보드](/img/ESP8266-ESP-12E-chip-pinout-gpio-pin.png)
***
# [추가 라이브러리]
### [WiFiManager](https://github.com/tzapu/WiFiManager)
* Wifi 설정 값 변경
```
```
### [WebSocketSerialMonitor](https://github.com/tzapu/WebSocketSerialMonitor)
* 웹 소켓 사용
* [예제1)](http://tzapu.github.io/WebSocketSerialMonitor/)
***
## [즐겨찾기]
* https://cafe.naver.com/lsg20004/873
* https://cafe.naver.com/lh0006/2292
***
### 내부 VCC 측정 방법 (A0 핀 연결 X)
* 외부 전압 분배 회로 없이 ESP8266 칩 자체의 공급 전압을 확인하고 싶다면 아래 코드.
* 이 경우 A0 핀은 아무것도 연결하지 않은 상태(Floating)여야 합니다
```
ADC_MODE(ADC_VCC); // 함수 밖 상단에 선언
void loop() {
  float vcc = ESP.getVcc() / 1000.0; // mV 단위를 V로 변환
  Serial.print("VCC Voltage: ");
  Serial.println(vcc);
```