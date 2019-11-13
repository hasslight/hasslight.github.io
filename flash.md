# Flash Firmware

The following guide helps you flash HassLight LED controller with Apple HomeKit based firmware or Home Assistant MQTT based firmware.

> Please be aware that it's NOT necessary for you to flash the firmware. It comes with HomeKit based firmware by default.

Congratulations! If you are still reading this, I assume you are a professional and know what you are going to do. 
By using Home Assistant based firmware which usually means you want to have more flexibility in controlling your LED strip.

Have fun!

----

## Prerequesites 
1. Install [CH340G driver](https://sparks.gogo.co.nz/ch340.html) if you have never done this on your OS.
2. Download [HassLightFlasher.exe](https://github.com/hasslight/hasslightflasher/releases/download/v4.0-mod/HassLightFlasher-4.0-x64.exe) for Windows or [HassLightFlasher.dmg](https://github.com/hasslight/hasslightflasher/releases/download/v4.0-mod/HassLightFlasher-4.0.dmg) for Mac 
3. Choose the firmware to download  

Integration | Product | Color Order |  Is Default | Length  | Firmware 
--          | --      | --          | --          | --      | --  
HomeKit | Holiday String (5V)  | RGB | 1 | 5-10 Meter | [Download](https://github.com/hasslight/hasslight.github.io/releases/download/v1.0/homekit_holiday_5V_100_RGB.bin) 
HomeKit | Mood LED Strip (12V) | BRG | 1 | 5 Meter | [Download](https://github.com/hasslight/hasslight.github.io/releases/download/v1.0/homekit_mood_12V_300_BRG.bin) 
HomeKit | Mood LED Strip (12V) | BRG | 0 | 10 Meter | [Download](https://github.com/hasslight/hasslight.github.io/releases/download/v1.0/homekit_mood_12V_600_BRG.bin) 
HomeKit | Mood LED Strip (12V) | GRB | 0 | 5 Meter | [Download](https://github.com/hasslight/hasslight.github.io/releases/download/v1.0/homekit_mood_12V_300_GRB.bin) 
HomeKit | Mood LED Strip (12V) | GRB | 0 | 10 Meter | [Download](https://github.com/hasslight/hasslight.github.io/releases/download/v1.0/homekit_mood_12V_600_GRB.bin) 
HomeAssistant | Holiday String (5V) | RGB | 0 | 5-10 Meter | [Download](https://github.com/hasslight/hasslight.github.io/releases/download/v1.0/ha_mqtt_holiday_5V_100_RGB.bin) 
HomeAssistant | Mood LED Strip (12V) | BRG | 0 | 5 Meter | [Download](https://github.com/hasslight/hasslight.github.io/releases/download/v1.0/ha_mqtt_mood_12V_300_BRG.bin) 
HomeAssistant | Mood LED Strip (12V) | GRB | 0 | 5 Meter | [Download](https://github.com/hasslight/hasslight.github.io/releases/download/v1.0/ha_mqtt_mood_12V_300_GRB.bin) 
WLED | Holiday String (5V)  | ANY | 0 | 5-10 Meter | [Download](https://github.com/hasslight/hasslight.github.io/releases/download/v1.0/hasslight-wled-0.8.6.bin)
WLED | Mood LED Strip (12V) | ANY | 0 | 5-10 Meter | [Download](https://github.com/hasslight/hasslight.github.io/releases/download/v1.0/hasslight-wled-0.8.6.bin)

 *If you are using Linux command*, you need 2 additional files [rboot.bin](https://github.com/hasslight/hasslight.github.io/releases/download/v1.0/rboot.bin) and [blank_config.bin](https://github.com/hasslight/hasslight.github.io/releases/download/v1.0/blank_config.bin) for HomeKit firmware

> When extending the LED strip longer, check this [Extend LED Strip](/extend)

## Apple HomeKit


### Mac / Windows

* Make sure jumper header set on **0-hkit**  
 ![](../imgs/jumper_header.jpg ':size=300')

* Start HassLightFlasher
   * Choose serial port, click refresh if not seen
   * Choose the firmware.bin which you just download 
   * Click "Flash" button, a successful flash looks like the example pictures below
* Next, follow the [Use Apple HomeKit](guide) to config

![](/imgs/hasslightflasher-mac.png)

![](/imgs/hasslightflasher-win.png)


### Linux

* Install esptool and then flash

    $ pip install esptool   
    $ esptool.py --chip esp8266 -p /dev/cu.wchusbserial620 --baud 115200 write_flash -fs detect -fm dio -ff 40m 0x0 rboot.bin 0x1000 blank_config.bin 0x2000 holiday_firmware.bin 

* Next, follow the [Use Apple HomeKit](guide) to config
----

## Home Assistant
### Mac / Windows

* Make sure jumper header set on **0-hass**  
 ![](../imgs/jumper_header_hass.jpg ':size=300')

* Start HassLightFlasher
   * Choose serial port, click refresh if not seen
   * Choose the firmware.bin which you just download 
   * Toggle "Default / Home Assistant / MQTT" integration
   * Click "Flash" button, a successful flash looks like the example pictures below
* Next, follow the [Use Home Assistant](guide-ha) to config

![](/imgs/hasslightflasher-mac-ha.png)

![](/imgs/hasslightflasher-win-ha.png)

### Linux

* Install esptool and then flash

    $ pip install esptool   
    $ esptool.py --chip esp8266 -p /dev/cu.wchusbserial620 --baud 115200 write_flash -fs detect -fm dio -ff 40m 0x0 holiday_firmware.bin 

* Next, follow the [Use Home Assistant](guide-ha) to config

## WLED
### Mac / Windows

* Make sure jumper header set on **0-hkit**  
 ![](../imgs/jumper_header.jpg ':size=300')

* Start HassLightFlasher
   * Choose serial port, click refresh if not seen
   * Choose the firmware.bin which you just download 
   * Toggle "Default / Home Assistant / MQTT" integration
   * Click "Flash" button, a successful flash looks like the example pictures below
* Next, follow the [Use WLED](guide-wled) to config

![](/imgs/hasslightflasher-mac-ha.png)

![](/imgs/hasslightflasher-win-ha.png)

### Linux

* Install esptool and then flash

    $ pip install esptool   
    $ esptool.py --chip esp8266 -p /dev/cu.wchusbserial620 --baud 115200 write_flash -fs detect -fm dio -ff 40m 0x0 hasslight-wled-*.bin 

* Next, follow the [Use WLED](guide-wled) to config