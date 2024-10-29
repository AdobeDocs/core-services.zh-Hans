---
description: 了解 Adobe Experience Cloud 中的 Adobe Analytics Cookie。
solution: Analytics
title: Adobe Analytics Cookies
uuid: e2d3d61d-2708-48b2-a7e6-2331f2aed8e0
feature: Cookies
topic: Administration
role: Admin
level: Experienced
exl-id: bc8ce894-f98c-4475-8a07-d74ae76f7451
source-git-commit: 5905644c2de154da77f33ae486818b5bede418df
workflow-type: tm+mt
source-wordcount: '379'
ht-degree: 16%

---

# Adobe Analytics Cookie

Adobe Analytics 使用 Cookie 区分来自不同浏览器的请求，并存储应用程序以后可以使用的有用信息。还可使用它们将浏览信息与客户记录相关联。

Analytics使用Cookie匿名定义新访客、帮助分析点击流数据并跟踪网站上的历史活动，如对特定营销活动的响应或销售周期的长度。

| Cookie 名称 | 过期 | 大小 | 位置 | 描述 |
| --- | --- | --- | --- | --- |
| **`s_ecid`** | 2 年 | 45 字节 | 第一方 | 存储Experience CloudID (ECID)或MID。 由HTTP响应设置。 MID以`s_ecid=MCMID`格式存储。 在客户端设置AMCV Cookie后设置。 它允许永久性的第一方ID跟踪，并在AMCV Cookie过期时用作参考ID。 此Cookie不适用于第三方Cookie实施。 `SameSite`设置为“Lax”。 |
| **`s_cc`** | 会话 | 4 字节 | 第一方 | 确定是否启用Cookie。 由JavaScript设置。 |
| **`s_sq`** | 会话 | 100-200字节 | 第一方 | 由Activity Map使用。 它包含有关访客点击的上一个链接的信息。 由JavaScript设置。 |
| **`s_vi`** | 2 年 | 44 字节 | 第一方，或`*.omtrdc.net` （第三方） | 存储唯一的访客ID和时间戳。 由HTTP响应设置。 每个访客ID均与Adobe服务器上的一个访客资料关联。 访客资料在处于1年的非活动状态之后会被删除，这与任何访客ID Cookie过期日期无关。 当`SameSite`为“None”且连接为HTTPS时，设置`Secure`标志。 对于第一方Cookie，`SameSite`默认为“Lax”。 使用第三方Cookie时，`SameSite`为“无”，例如在`omtrdc.net`或`2o7.net`上。 使用单个CNAME跟踪多个域或属性时，将`SameSite`设置为“无”。 |
| **`s_fid`** | 2 年 | 33 字节 | 第一方 | 存储后备唯一访客ID和时间戳。 如果由于第三方Cookie限制而无法设置标准`s_vi` Cookie，则由JavaScript设置。 不用于第一方Cookie实施。 |
| **`s_ac`** | 立即 | 1字节 | 第一方 | 帮助确定设置AppMeasurementCookie的正确域。 包含静态值`"1"`。 设置此Cookie后，将立即将其删除。 |

{style="table-layout:auto"}

## 插件设置的 Cookie

某些实施使用插件，这些插件是为Analytics提供附加功能的代码片段。 这些插件可以设置以上未列出的Cookie。 有关可用插件及其设置的Cookie的列表，请参阅[Analytics插件概述](https://experienceleague.adobe.com/en/docs/analytics/implementation/vars/plugins/impl-plugins)。
