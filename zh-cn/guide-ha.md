# 用户手册

HassLight LED 控制器可让您将LED灯条连接到智能家居，并通过"Siri" 或 "Alexa" 或连接到Home Assistant的任何其他智能音箱进行控制。

目前，我们支持三种集成方式。 
1. 连接到Apple HomeKit（iOS 家庭 APP）
2. 连接到Home Assistant
3. 连接到WLED（WLED APP for iOS and Android, Alexa, MQTT etc.）

默认情况下，它带有基于HomeKit的固件，可与iOS 家庭 APP进行交互。
我们还非常容易刷写基于MQTT的固件，以便与Home Assistant进行交互。 当然，您可以来回切换两种方式。 参考 [刷写固件](/zh-cn/flash).

----

## 步骤

 与基于HomeKit的固件不同，基于Home Assistant的固件要求您首先配置WiFi和MQTT设置，然后才能使用按钮单击。
 此后，即使MQTT连接不可用，脱机按钮控制也始终起作用。 **这可能会随着固件升级而改变。**

1. 将控制器连接到家庭WiFi网络并配置MQTT设置
   **请截屏，下一步需要设备ID（WiFi名称：hasslight_xxxxxx）**

<!-- tabs:start -->

#### ** 1 **

无线网络设置

![](../imgs/ha/config_ha_1.jpg ':size=480')

#### ** 2 **

选取网络... -> hasslight_xxxxxx  

![](../imgs/ha/config_ha_2.jpg ':size=480')

#### ** 3 **

配置无线网 

![](../imgs/ha/config_ha_3.jpg ':size=480')

#### ** 4 **

输入MQTT IP，PORT，USERNAME，PASSWORD
大多数用户使用Hass.io Mosquito插件，如果您使用的是NAS Docker，应该知道怎么安装启动MQTT Broker。

![](../imgs/ha/config_ha_4.jpg ':size=480')

#### ** 5 **

如果设置正确，则您的LED灯条应该现在已经打开，控制器将向您的MQTT服务器发布可用消息，因此现在您可以使用按钮切换开/关。

![](../imgs/ha/config_ha_5.jpg ':size=480')

<!-- tabs:end -->


2. 与 Home Assistant 集成

  2.1 复制 [example.yaml](./zh-cn/hass.md?id=home-assistant-example-configuration) 并且 替换 device_id，第一步需要您截图的那个就是

  2.2  
  **方法 1:** 直接粘贴到 *configuration.yaml*  
  **方法 2:** 如果您启用packages功能，可以保存为 **hasslight.yaml** 然后放置到packages目录即可

  ```
  homeassistant:    
      packages: !include_dir_named packages  
  ```

  2.3 打开 Home Assistant 转到 配置-> 服务控制-> 检查配置（如果配置有效），然后 重新启动

  2.4 在 Home Assistant 主页 或 未使用的实体 里找到它，现在您已可以完全控制它了

  ![](../imgs/ha/config_ha_6.jpg ':size=680')
  