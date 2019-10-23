# 用户手册

HassLight LED 控制器可让您将LED灯条连接到智能家居，并通过"Siri" 或 "Alexa" 或连接到Home Assistant的任何其他智能音箱进行控制。

目前，我们支持两种集成方式。 
1. 连接到Apple HomeKit（iOS 家庭 APP）
2. 连接到Home Assistant

默认情况下，它带有基于HomeKit的固件，可与iOS 家庭 APP进行交互。
我们还非常容易刷写基于MQTT的固件，以便与Home Assistant进行交互。 当然，您可以来回切换两种方式。 参考 [刷写固件](flash).

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

5. 更改LED效果/速度等

6. **（可选）**如果WiFi发生更改（新的无线路由器/更改的密码等），请重置控制器。

   **按住按钮** 6秒钟以重置控制器，LED灯条将闪烁3轮以表明已完成重置。 然后回到步骤3将其重新连接。

----