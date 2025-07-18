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
source-git-commit: d3a559ca2f7963256d48a25cd51099edb5e3fe76
workflow-type: tm+mt
source-wordcount: '535'
ht-degree: 11%

---

# Adobe Analytics Cookie

Adobe Analytics 使用 Cookie 区分来自不同浏览器的请求，并存储应用程序以后可以使用的有用信息。还可使用它们将浏览信息与客户记录相关联。

Analytics使用Cookie匿名定义新访客、帮助分析点击流数据并跟踪网站上的历史活动，如对特定营销活动的响应或销售周期的长度。

| Cookie 名称 | 过期 | 大小 | 位置 | 描述 |
| --- | --- | --- | --- | --- |
| **`s_ecid`** | 13 个月 | 45 字节 | 第一方 | 存储Experience Cloud ID (ECID)或MID。 由HTTP响应设置。 MID以`s_ecid=MCMID`格式存储。 在客户端设置AMCV Cookie后设置。 它允许永久性的第一方ID跟踪，并在AMCV Cookie过期时用作参考ID。 `SameSite`设置为“Lax”。 如果您使用Web SDK实施Adobe Analytics，则Cookie过期时间设置为2年；但是，大多数现代浏览器都会将过期时间截断为13个月。 |
| **`s_cc`** | 会话 | 4 字节 | 第一方 | 确定是否启用Cookie。 由JavaScript设置。 |
| **`s_sq`** | 会话 | 100-200字节 | 第一方 | 由Activity Map使用。 它包含有关访客点击的上一个链接的信息。 由JavaScript设置。 |
| **`s_vi`** | 2 年 | 44 字节 | 第一方，或`*.omtrdc.net` （第三方） | 存储唯一的访客ID和时间戳。 由HTTP响应设置。 每个访客ID都与Adobe服务器上的一个访客资料关联。 访客资料在处于1年的非活动状态之后会被删除，这与任何访客ID Cookie过期日期无关。 当`Secure`为“None”且连接为HTTPS时，设置`SameSite`标志。 对于第一方Cookie，`SameSite`默认为“Lax”。 使用第三方Cookie时，`SameSite`为“无”，例如在`omtrdc.net`或`2o7.net`上。 使用单个CNAME跟踪多个域或属性时，将`SameSite`设置为“无”。 |
| **`s_fid`** | 2 年 | 33 字节 | 第一方 | 存储后备唯一访客ID和时间戳。 如果由于第三方Cookie限制而无法设置标准`s_vi` Cookie，则由JavaScript设置。 不用于第一方Cookie实施。 |
| **`s_ac`** | 立即 | 1字节 | 第一方 | 帮助确定正确域以设置AppMeasurement Cookie。 包含静态值`"1"`。 设置此Cookie后，将立即将其删除。 |

## 插件设置的 Cookie

某些实施使用插件，这些插件是为Analytics提供附加功能的代码片段。 这些插件可以设置以上未列出的Cookie。 有关可用插件及其设置的Cookie的列表，请参阅[Analytics插件概述](https://experienceleague.adobe.com/en/docs/analytics/implementation/vars/plugins/impl-plugins)。

## 删除Analytics Cookie的后果

如果访客删除其Analytics Cookie，请考虑以下事项：

* **访客标识丢失：**&#x200B;删除Cookie时，Adobe Analytics无法识别回访访客。 用户下次访问您的网站时，即会被计为新访客。 [跨设备分析](https://experienceleague.adobe.com/en/docs/analytics/components/cda/overview)可以帮助减轻这种影响。
* **会话连续性已中断：**&#x200B;任何基于会话的或多访问分析（如归因或转化跟踪）均被中断。 Cookie删除后发生的事件和转化不能由同一用户关联到以前的活动。
* **Personalization和分段受到影响：**&#x200B;基于访客历史记录或行为的区段或个性化体验将被重置，因为以前的数据不再与其当前访问关联。
* **跨域跟踪被中断：**&#x200B;对于第三方Cookie，删除它们会阻止Adobe Analytics链接您拥有的多个域中的用户活动。
