# Flash Firmware

The following guide helps you flash HassLight LED controller with Apple Homekit based firmware or Home Assistant MQTT based firmware.

> Congratulations! If you are reading this, I assume you are a professional and know what you are going to do. Have fun!

----

## Apple Homekit

> Again, please be aware that it's NOT necessary for you to flash the firmware, only if you are a fanatic and want to switch between homekit and home assistant. 

### Mac / Windows

1. Install [CH340G driver](https://sparks.gogo.co.nz/ch340.html) if you never have done this on your OS.
2. Download [HassLightFlasher.exe](HassLightFlasher-4.0.exe) for Windows or [HassLightFlasher.dmg](HassLightFlasher-4.0.dmg) for Mac 
3. Download [holiday_firmware.bin]() or [mood_firmware.bin]() 
4. Start HassLightFlasher
   * Choose serial port, click refresh if not seen
   * Choose the firmware.bin which you just download 
   * Click "Flash" button, a successful flash looks like the example pictures below

![](./imgs/hasslightflasher-mac.png)

![](./imgs/hasslightflasher-win.png)


### Linux

1. Install [CH340G driver](https://sparks.gogo.co.nz/ch340.html) if you never have done this on your OS.
2. Download [rboot.bin]() and [blank_config.bin]()
3. Download [holiday_firmware.bin]() or [mood_firmware.bin]() 
4. Install esptool and then flash

    $ pip install esptool   
    $ esptool.py --chip esp8266 -p /dev/cu.wchusbserial620 --baud 115200 write_flash -fs detect -fm dio -ff 40m 0x0 rboot.bin 0x1000 blank_config.bin 0x2000 holiday_firmware.bin 

----

## Home Assistant
### Mac / Windows
### Linux