---
title: LightCVM and DB in Tencent Cloud
date: 2022-03-05 16:30:55
tags:  CloudServer
---
## Scene
- 在使用轻量级应用服务器的时候发现连接不上数据库
- 查阅得知,腾讯云内部轻量服务器和云数据库默认内网是不通的
<!-- more -->

## Solution
- 到轻量级应用服务器 console 选择 内网互联 tab , 然后选择区域 “关联云联网” 
- ![](/images/lightCVMAndDBinTencentCloud/Snipaste_2022-03-05_16-38-12.png)
- 填写信息建立关联后,到 私有网络的云联网中进行确认配置即可
- ![](/images/lightCVMAndDBinTencentCloud/Snipaste_2022-03-05_16-41-01.png)
- 值得注意的一点是，**云联网的设备是需要付费的，但是如果设备在同一个地域就不需要收费**（如：上海一区和上海五区是同一个地域）
  
## Other 
- 👉 [内网互联](https://cloud.tencent.com/document/product/1207/56847)
- 👉 [云联网](https://cloud.tencent.com/document/product/877)
