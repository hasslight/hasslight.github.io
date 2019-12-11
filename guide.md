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

5. **(iOS 13 Only)** How to change the Group & Stacked "Single Tile" to "Seperate Tile", aka. iOS 13 style to iOS 12 style

  First tap "HASSLIGHT", then scrol down to the bottom, tap "Show as Seperate Tiles", then you'll see picture 5.3 which is the iOS 12 style.  

  To switch it back to "Single Tile", the steps are the same. First long tap any "Tile", then scrol down to the bottom, then tap "Show as Single Tile". 

5.1 | 5.2 | 5.3 
-- | -- | -- 
![](/imgs/ios/single_tile.jpg ':size=400') | ![](/imgs/ios/single_tile_change.jpg ':size=400') | ![](/imgs/ios/seperate_tile.jpg ':size=400') 


6. Change the LED color / effect / speed etc.

  Tiles info:  
  **HASSLIGHT**: The light bulb, The LED Strip, controls color, brightness  
  **A HASSLIGHT FX SPEED**: The virtual light bulb, controls 52 hidden effects, when change this tile's brightness it actually changes the current animation speed  

  **Christmas**: an animation effect, plus brightness  
  **Fireworks**: an animation effect, plus brightness  
  **Halloween**: an animation effect, plus brightness  
  **Rainbow**: an animation effect, plus brightness  
  **Twinkle**: an animation effect, plus brightness  
  **Warm White**: an animation effect, plus brightness  

6.1. How to change the LED color or brightness?  

  First turn off any effect which may be on. Then tap the "HASSLIGHT" tile to set the solid color mode.
  Next "Long tap" the "HASSLIGHT" title to edit the color you need. Steps are shown below.

  Changing the brightness is much simpler, just "Tap and Scroll" the brightness bar up and down. (the step2 pictures)

&nbsp; | Step 1 | Step 2 | Step 3 
-- | -- | -- | -- 
Seperate Tile on iOS 13 or iOS 12 | ![](/imgs/ios/color_12.jpg ':size=400') | ![](/imgs/ios/color_12_1.jpg ':size=400') | ![](/imgs/ios/color.jpg ':size=400') 
Single Tile on iOS 13 | ![](/imgs/ios/color_13.jpg ':size=400') | ![](/imgs/ios/color_13_1.jpg ':size=400') | ![](/imgs/ios/color.jpg ':size=400') 

6.2. How to change the LED effects?  
  

  **The Preset Effects**

  Changing the preset effects is quite abvious, just "Tap" Christmas, Fireworks, Halloween, Rainbow, Twinkle, Warm White 

  **The Hidden Effects**  

  There are 52 hidden effects, you can access them by edit "A HASSLIGHT FX SPEED" color, the edit steps are similar to edit the solid color, only difference is that current tile is "A HASSLIGHT FX SPEED". 
  
  There is no corresponding text shown the effect name though. You can just see how the LED strip response to your change.
  
  Steps are shown below.

iOS 12 / Seperate Tile | iOS 13 Single Tile | Edit Effect | Effects color wheel 
-- | -- | -- | -- 
![](/imgs/ios/effect12_1.jpg ':size=400') | ![](/imgs/ios/effect13_1.jpg ':size=400') | ![](/imgs/ios/effect2.jpg ':size=400') | ![](/imgs/ios/effect3.jpg ':size=400')

7. **(Optional)** Reset the controller in case of WiFi changes (new wireless router / changed password etc.)

  **Press and Hold** for 6 seconds to reset the controller, the LED strip will blink for 3 rounds to indicate that reset is done. Then go back to step 3 to connect it back.

----