# iRuxuStreamingIndicator
通过 B 站弹幕服务器拉取直播间状态，上、下播时通过 MQTT 消息进行通知，下位机（基于 ESP8266 与 [ESPHome](https://github.com/esphome/esphome) 固件）接收到消息后闪灯发音提示

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
          |             |--------- PWM -------> Buzzer
 [ ESP8266 (ESPHome) ] -|------- OneWire -----> Acrylic Light Diffuser
                        |<-------- DI --------- Touchkey
```
# 下位机
是个老坑，本来打算魔改[这个玩意](https://item.taobao.com/item.htm?spm=a230r.1.14.18.36a23bbfKBXWqU&id=635493431852)后来坑了，差不多的东西直接拿过来用

https://oshwhub.com/whc2001/nightlightannunciator

# 上位机
> WIP..
