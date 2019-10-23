# User Manual

HassLight LED Controller let you connect LED strip to your smart home, and control it via "Siri" or "Alexa" or any other smart speakers connected to Home Assistant. 

For now we support three ways of integrating. 
1. Connect with Apple HomeKit (iOS Home APP)
2. Connect with Home Assistant
3. Connect with WLED (WLED APP for iOS and Android, Alexa, MQTT etc.)  

By default, it comes with the HomeKit based firmware to interact with iOS Home APP.
We also made it quite easy to flash the MQTT based firmware, in order to interact with Home Assistant. And of course you can switch the integration ways back and forth. See [Flash firmware](flash).

----

## Guide

> For simplicity "the HassLight LED Controller" hereinafter referred to as "the controller" 

1. Connect the LED strip to the controller's female socket
2. Connect the power cable to the controller. 
 
   **Single click** the button on the controller to toggle it on/off.  
   **Double click** the button on the controller to switch the build in themes. (White, Blink, Christmas, Halloween, Rainbow, Twinkle)

3. Use an iPhone/iPad to configure the controller to connect to your home WiFi network.

<!-- tabs:start -->

  #### ** 1 **

  Open Settings -> WLAN

  ![](/imgs/ios/ios_wifi_1.jpg ':size=400')

  #### ** 2 **

  CHOOSE A NETWORK -> HassLight-XXXXXX 

  ![](/imgs/ios/ios_wifi_2.jpg ':size=400')
  
  #### ** 3 **

  Join HassLight to your Home WiFi

  ![](/imgs/ios/ios_wifi_3.jpg ':size=400')

  #### ** 4 **

  Wait for about 10 seconds, then iOS will automatically connect back to your Home WiFi

  ![](/imgs/ios/ios_wifi_4.jpg ':size=400')

<!-- tabs:end -->

4. Pair it in iOS Home APP

<!-- tabs:start -->

  #### ** 1 **

  Open Home App, Click "+" on top right, Choose "Add Accessory"

  ![](/imgs/ios/homekit_1.jpg ':size=400')

  #### ** 2 **

  Add by Scan QRCode below, when see prompt "UnCertified Accessory", Click "Add Anyway"

  2.1 | 2.2 | 2.3 | 2.4
  --  | --  | --  | --
  ![](/imgs/ios/homekit_2_1.jpg ':size=400') | ![](/imgs/ios/homekit_2_2.jpg ':size=400') | ![](/imgs/ios/homekit_2_3.jpg ':size=400') | ![](/imgs/ios/homekit_2_4.jpg ':size=400')

  The QRCode  
  ![](/imgs/qrcode.png ':size=400')

  #### ** 3 **

  Add Accessory one by one, just click **Next** all the way till the end.   
  By the way the LED strip will blink 3 times for "Indentify Accessory", since it's just one phicical device, thus the effects are virtual buttons for convenience.

  **For iOS13**:  
  ![](/imgs/ios/homekit_3_ios13.jpg ':size=400') 

  **For iOS12**:  

  ~ | ~ | ~ | ~
  --  | --  | --  | --
  ![](/imgs/ios/homekit_3_1.jpg ':size=400') | ![](/imgs/ios/homekit_3_2.jpg ':size=400') | ![](/imgs/ios/homekit_3_3.jpg ':size=400') | ![](/imgs/ios/homekit_3_4.jpg ':size=400')
  ![](/imgs/ios/homekit_3_5.jpg ':size=400') | ![](/imgs/ios/homekit_3_6.jpg ':size=400') | ![](/imgs/ios/homekit_3_7.jpg ':size=400') | ![](/imgs/ios/homekit_3_8.jpg ':size=400')

  #### ** 4 **

  Your holiday or mood LED strip is ready.
  
  **For iOS13**:  

  ~ | ~ 
  --  | -- 
  ![](/imgs/ios/homekit_4_1_ios13.jpg ':size=400') | ![](/imgs/ios/homekit_4_2_ios13.jpg ':size=400') 


  **For iOS12**:  
  ![](/imgs/ios/homekit_4.jpg ':size=400') 

<!-- tabs:end -->

5. Change the LED effect / speed etc.

6. **(Optional)** Reset the controller in case of WiFi changes (new wireless router / changed password etc.)

  **Press and Hold** for 6 seconds to reset the controller, the LED strip will blink for 3 rounds to indicate that reset is done. Then go back to step 3 to connect it back.

----