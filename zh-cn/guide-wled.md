# 用户手册

HassLight LED 控制器可让您将LED灯条连接到智能家居，并通过"Siri" 或 "Alexa" 或连接到Home Assistant的任何其他智能音箱进行控制。

目前，我们支持三种集成方式。 
1. 连接到Apple HomeKit（iOS 家庭 APP）
2. 连接到Home Assistant
3. 连接到WLED（WLED APP for iOS and Android, Alexa, MQTT etc.）

默认情况下，它带有基于HomeKit的固件，可与iOS 家庭 APP进行交互。
我们还非常容易刷写基于MQTT的固件，以便与Home Assistant进行交互。 当然，您可以来回切换两种方式。 参考 [刷写固件](zh-cn/flash).

----

## HassLight-WLED
简单来说：HassLight LED控制器可以[刷 WLED 固件](zh-cn/flash)。  
WLED是一个开源项目，实现了在ESP8266/ESP32上控制NeoPixel系列灯带的Web服务。本固件是基于WLED做的适配定制，包含适当的修改，有WLED的大部分功能，然后大家可以使用WLED APP控制HassLight灯带产品。

WLED功能强大，本身的配置项非常的多，这里不会一一列举，使用方法主要说一下配网和效果切换的控制，更多功能可以参考WLED项目主页。有问题也可以在我们的技术交流群里提问。

### 功能简介
* 渐亮、渐暗
* 80 多种特效
* 噪声效果 和 多种预设色盘
* 移动端 和 网页版 配置
* 支持预设效果
* 支持宏功能，直接触发调用API
* 按钮行为自定义
* 可配置自动亮度限制更安全
* OTA 升级

### 控制接口
* Android / iOS APP, 应用商店搜索 WLED
* JSON / HTTP API
* MQTT
* Alexa voice control (亮度调节、颜色)
* 同步到飞利浦Hue灯带
* 同步多个WLED设备
* 简单的定时、计划执行

### 界面预览

 ![](../imgs/wled/settings.png ':size=600')

 ![](../imgs/wled/settings2.png ':size=600')



## 使用方法

> 为了简单起见，以下将"HassLight LED控制器"称为"控制器"

1. 将LED灯条连接到控制器的母座。
2. 将电源线连接到控制器。
 
    **单击**控制器上的按钮以将其打开/关闭。  
    **双击**控制器上的按钮以切换预设效果。

3. 使用iPhone / iPad将控制器配置连接到您的家庭WiFi网络。

<!-- tabs:start -->

  #### ** 1 **

  打开设置 -> 无线局域网

  ![](../imgs/wled/ios_wifi_1.jpg ':size=400')

  #### ** 2 **

  选取网络... -> HassLight-WLED-AP 

  ![](../imgs/wled/ios_wifi_2.jpg ':size=400')
  
  #### ** 3 **

  配置 HassLight 加入您的家庭Wifi

  ![](../imgs/wled/ios_wifi_3.jpg ':size=400')

  #### ** 4 **

  等待约10秒钟，然后iOS将自动连接回您的家庭WiFi (此时控制器应该也成功连接到了您的家庭Wifi)

  ![](../imgs/wled/ios_wifi_4.jpg ':size=400')

<!-- tabs:end -->

4. 使用WLED APP发现灯带

5. 更改LED效果/速度等

6. **（可选）**如果WiFi发生更改（新的无线路由器/更改的密码等），请重置控制器。

   **按住按钮** 6秒钟以重置控制器，LED灯条将闪烁3轮以表明已完成重置。 然后回到步骤3将其重新连接。

----