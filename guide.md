# User Manual

HassLight LED Controller let you connect LED strip to your smart home, and control it via "Siri" or "Alexa" or any other smart speakers connected to Home Assistant. 

For now we support two ways of integrating. 
1. Connect to Apple Homekit (iOS Home APP)
2. Connect to Home Assistant 

By default, it comes with the homekit based firmware to interact with iOS Home APP.
We also made it quite easy to flash the MQTT based firmware, in order to interact with Home Assistant. And of course you can switch the two ways back and forth. See [Flash firmware](flash).

----

## Apple Homekit

> For simplicity "the HassLight LED Controller" hereinafter referred to as "the controller" 

1. Connect the LED strip to the controller's female socket
2. Connect the power cable to the controller. 
 
   **Single click** the button on the controller to toggle it on/off.  
   **Double click** the button on the controller to switch the build in themes. (White, Blink, Christmas, Halloween, Rainbow, Twinkle)

3. You will need an iPhone/iPad to configure the controller to connect to your home WiFi network.

<!-- tabs:start -->

    #### ** Open Settings **

    Open Settings -> WLAN

    #### ** Choose a Network **

    CHOOSE A NETWORK -> HassLight-XXXXXX 

    #### ** Config HassLight's Home WiFi**

    Join HassLight to your Home WiFi

    #### ** Wait 10 seconds **

    Wait for iOS to automatically connect back to your Home WiFi

<!-- tabs:end -->

4. Pair it in iOS Home APP

<!-- tabs:start -->

    #### ** Open Home App **

    Open Home App, Click "+" on top right, Choose "Add Accessory"

    #### ** Scan QRCode **

    CHOOSE A NETWORK -> HassLight-XXXXXX 

    #### ** Next, Next **

    Join HassLight to your Home WiFi

    #### ** Done **

    Wait for iOS to automatically connect back to your Home WiFi

<!-- tabs:end -->

5. **(Optional)** Reset the controller in case of WiFi changes (new wireless router / changed password etc.)

  **Press and Hold** for 6 seconds to reset the controller, the LED strip will blink for 3 rounds to indicate that reset is done. Then go back to step 3 to connect it back.

----

## Home Assistant

  **This may change in furture with firmware upgrade.** Unlike homekit based firmware, the Home Assistant based firmware requires you to configure WiFi and MQTT settings first before you can use button click. 
  After that, even if MQTT connection unavailable, offline button control is always functional. 

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
