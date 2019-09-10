# User Manual

HassLight LED controller let you connect LED strip to your smart home, and control it via "Siri" or "Alexa" or any other smart speakers connected to Home Assistant. 

For now we support two ways of integrating. 
1. Connect to iOS Home APP
2. Connect to Home Assistant 

By default, it comes with the homekit based firmware to interact with iOS Home APP.
We also made it quite easy to flash the MQTT based firmware, in order to interact with Home Assistant. And of course you can switch the two ways back and forth. 


## iOS "Home APP"
### Setup Steps

1. Connect the HassLight controller to your home WiFi network
2. Pair it in iOS Home APP
3. (Optional) reset the the HassLight controller in case of WiFi changes (new wireless router / changed password etc.)

### Flash firmware

#### Windows
1. Install [CH340G driver](https://sparks.gogo.co.nz/ch340.html) if you never did this on your system.
2. Download ["Flash Download Tools (ESP8266 & ESP32)"](https://www.espressif.com/sites/default/files/tools/flash_download_tools_v3.6.7_1.zip) from Espressif.com
3. Download [rboot.bin](), [blank_config.bin](), [hasslight_firmware_latest.bin]() 
4. Start Flash Download Tools

#### Mac


## Home Assistant
### Setup Steps
### Flash firmware