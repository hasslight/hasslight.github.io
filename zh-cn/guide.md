# 用户手册

HassLight LED 控制器可让您将LED灯条连接到智能家居，并通过"Siri" 或 "Alexa" 或连接到Home Assistant的任何其他智能音箱进行控制。

目前，我们支持三种集成方式。 
1. 连接到Apple HomeKit（iOS 家庭 APP）
2. 连接到Home Assistant
3. 连接到WLED（WLED APP for iOS and Android, Alexa, MQTT etc.）

默认情况下，它带有基于HomeKit的固件，可与iOS 家庭 APP进行交互。
我们还非常容易刷写基于MQTT的固件，以便与Home Assistant进行交互。 当然，您可以来回切换两种方式。 参考 [刷写固件](zh-cn/flash).

----

## 步骤

> 为了简单起见，以下将"HassLight LED控制器"称为"控制器"

1. 将LED灯条连接到控制器的母座。
2. 将电源线连接到控制器。
 
    **单击**控制器上的按钮以将其打开/关闭。  
    **双击**控制器上的按钮以切换预设主题。 （白色，圣诞节，万圣节，彩虹，闪烁，眨眼）

3. 使用iPhone / iPad将控制器配置连接到您的家庭WiFi网络。

<!-- tabs:start -->

  #### ** 1 **

  打开设置 -> 无线局域网

  ![](../imgs/ios/ios_wifi_1.jpg ':size=400')

  #### ** 2 **

  选取网络... -> HassLight-XXXXXX 

  ![](../imgs/ios/ios_wifi_2.jpg ':size=400')
  
  #### ** 3 **

  配置 HassLight 加入您的家庭Wifi

  ![](../imgs/ios/ios_wifi_3.jpg ':size=400')

  #### ** 4 **

  等待约10秒钟，然后iOS将自动连接回您的家庭WiFi (此时控制器应该也成功连接到了您的家庭Wifi)

  ![](../imgs/ios/ios_wifi_4.jpg ':size=400')

<!-- tabs:end -->

4. 在iOS 家庭 APP中添加配对

<!-- tabs:start -->

  #### ** 1 **

  打开 家庭 APP，单击右上角的"+"，选择"添加配件"

  ![](../imgs/ios/homekit_1.jpg ':size=400')

  #### ** 2 **

  通过扫描QRCode添加，当看到提示"未经认证的配件"时，单击"仍然添加"

  2.1 | 2.2 | 2.3 | 2.4
  --  | --  | --  | --
  ![](../imgs/ios/homekit_2_1.jpg ':size=400') | ![](../imgs/ios/homekit_2_2.jpg ':size=400') | ![](../imgs/ios/homekit_2_3.jpg ':size=400') | ![](../imgs/ios/homekit_2_4.jpg ':size=400')

  QRCode  
  ![](../imgs/qrcode.png ':size=400')

  #### ** 3 **

  逐一添加配件，只需单击**下一步**直至结束。 顺便说一下，LED灯条将闪烁3次以显示"识别"设备正常，因为它只是一个实体控制器，这些配件都是特效对应的虚拟按钮。

  **iOS 13**:  
  ![](../imgs/ios/homekit_3_ios13.jpg ':size=400') 

  **iOS 12**:  

  ~ | ~ | ~ | ~
  --  | --  | --  | --
  ![](../imgs/ios/homekit_3_1.jpg ':size=400') | ![](../imgs/ios/homekit_3_2.jpg ':size=400') | ![](../imgs/ios/homekit_3_3.jpg ':size=400') | ![](../imgs/ios/homekit_3_4.jpg ':size=400')
  ![](../imgs/ios/homekit_3_5.jpg ':size=400') | ![](../imgs/ios/homekit_3_6.jpg ':size=400') | ![](../imgs/ios/homekit_3_7.jpg ':size=400') | ![](../imgs/ios/homekit_3_8.jpg ':size=400')

  #### ** 4 **

  您的节日彩灯串或氛围灯条已准备就绪。

  **iOS 13**:  

  ~ | ~ 
  --  | -- 
  ![](../imgs/ios/homekit_4_1_ios13.jpg ':size=400') | ![](../imgs/ios/homekit_4_2_ios13.jpg ':size=400') 


  **iOS 12**:  
  ![](../imgs/ios/homekit_4.jpg ':size=400') 

<!-- tabs:end -->

5. **(iOS 13 Only)** How to change the Group & Stacked "Single Tile" to "Seperate Tile", aka. iOS 13 style to iOS 12 style

  First tap "HASSLIGHT", then scrol down to the bottom, tap "Show as Seperate Tiles", then you'll see picture 5.3 which is the iOS 12 style.  

  To switch it back to "Single Tile", the steps are the same. First long tap any "Tile", then scrol down to the bottom, then tap "Show as Single Tile". 

5.1 | 5.2 | 5.3 
-- | -- | -- 
![](../imgs/ios/single_tile.jpg ':size=400') | ![](../imgs/ios/single_tile_change.jpg ':size=400') | ![](../imgs/ios/seperate_tile.jpg ':size=400') 


6. 更改LED颜色/效果/速度等

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
Seperate Tile on iOS 13 or iOS 12 | ![](../imgs/ios/color_12.jpg ':size=400') | ![](../imgs/ios/color_12_1.jpg ':size=400') | ![](../imgs/ios/color.jpg ':size=400') 
Single Tile on iOS 13 | ![](../imgs/ios/color_13.jpg ':size=400') | ![](../imgs/ios/color_13_1.jpg ':size=400') | ![](../imgs/ios/color.jpg ':size=400') 

6.2. How to change the LED effects?  
  

  **The Preset Effects**

  Changing the preset effects is quite abvious, just "Tap" Christmas, Fireworks, Halloween, Rainbow, Twinkle, Warm White 

  **The Hidden Effects**  

  There are 52 hidden effects, you can access them by edit "A HASSLIGHT FX SPEED" color, the edit steps are similar to edit the solid color, only difference is that current tile is "A HASSLIGHT FX SPEED". 
  
  There is no corresponding text shown the effect name though. You can just see how the LED strip response to your change.
  
  Steps are shown below.

iOS 12 / Seperate Tile | iOS 13 Single Tile | Edit Effect | Effects color wheel 
-- | -- | -- | -- 
![](../imgs/ios/effect12_1.jpg ':size=400') | ![](../imgs/ios/effect13_1.jpg ':size=400') | ![](../imgs/ios/effect2.jpg ':size=400') | ![](../imgs/ios/effect3.jpg ':size=400')


7. **（可选）**如果WiFi发生更改（新的无线路由器/更改的密码等），请重置控制器。

   **按住按钮** 6秒钟以重置控制器，LED灯条将闪烁3轮以表明已完成重置。 然后回到步骤3将其重新连接。

----