# User Manual

HassLight LED Controller let you connect LED strip to your smart home, and control it via "Siri" or "Alexa" or any other smart speakers connected to Home Assistant. 

For now we support two ways of integrating. 
1. Connect to Apple Homekit (iOS Home APP)
2. Connect to Home Assistant 

By default, it comes with the homekit based firmware to interact with iOS Home APP.
We also made it quite easy to flash the MQTT based firmware, in order to interact with Home Assistant. And of course you can switch the two ways back and forth. See [Flash firmware](flash).

----

## Guide

  Unlike homekit based firmware, the Home Assistant based firmware requires you to configure WiFi and MQTT settings first before you can use button click. 
  After that, even if MQTT connection unavailable, offline button control is always functional.  **This may change in furture with firmware upgrade.**  

1. Connect the controller to your home WiFi network and configure MQTT settings  
  **Take a screenshot of your device id (WiFi name: hasslight_xxxxxx) which you'll need for next step**


<!-- tabs:start -->

#### ** 1 **

WiFi Settings  
![](./imgs/ha/config_ha_1.jpg ':size=480')

#### ** 2 **

CHOOSE A NETWORK -> hasslight_xxxxxx  

![](./imgs/ha/config_ha_2.jpg ':size=480')

#### ** 3 **

Configure WiFi  

![](./imgs/ha/config_ha_3.jpg ':size=480')

#### ** 4 **

Type in MQTT IP,PORT,USERNAME,PASSWORD  
Most users use Hass.io Mosquito Addon, If you are on NAS docker, you know what to do.  

![](./imgs/ha/config_ha_4.jpg ':size=480')

#### ** 5 **

If settings are correct, your LED strip should be ON by now, the controller will publish available message to your MQTT server, so now you can use button to toggle ON/OFF.  

![](./imgs/ha/config_ha_5.jpg ':size=480')

<!-- tabs:end -->


2. Configure Home Assistant  

  2.1 Copy the [example.yaml](./hass.md?id=home-assistant-example-configuration) and Replace the device id with yours.  

  2.2  
  **Option 1:** Paste into to *configuration.yaml*  
  **Option 2:** Save it as a **hasslight.yaml** and place into packages folder if enabled in *configuration.yaml*.

  ```
  homeassistant:    
      packages: !include_dir_named packages  
  ```

  2.3 Go to Config -> Server Control -> Check config, if valid then Restart Home Assistant

  2.4 Find it at Home Assistant Home or unused-entities, you have full control now

  ![](./imgs/ha/config_ha_6.jpg ':size=680')
  