# iRuxuStreamingIndicator
浮烟在直播吗

# 结构
```
[ Bilibili Danmaku Server ]
          |
      Prop. API
          |
  [ Monitor Script ]
          |
         MQTT
          |
   [ MQTT Broker ] 
         |
         |
        MQTT
         |
         |              |--------- PWM -------> Buzzer
 [ ESP8266 (ESPHome) ] -|------- OneWire -----> Acrylic Light Diffuser
                        |<-------- DI --------- Touchkey
```
