---
title: Adobe Experience Platform Web SDK Cookie
description: 了解Web SDK如何使用适用于您的实施的Cookie。
solution: Experience Cloud
feature: Cookies
topic: Administration
role: Admin
level: Experienced
exl-id: 14f06dc9-255e-4a6c-adec-471107cf202e
source-git-commit: d69af76f6deff4f2b73e67ee7b69b9fee1ee3a2e
workflow-type: tm+mt
source-wordcount: '290'
ht-degree: 1%

---

# Adobe Experience Platform Web SDK Cookie

Adobe Experience Platform Web SDK使用Cookie来存储特定于您的实施的值。

| 名称 | 最大年龄 | 大小 | 描述 |
|---|---|---|---|
| **kndctr_&lt;ORG_ID>_identity** | 34128000（395天） | 100-120字节（变量） | 存储ECID以及与ECID相关的其他信息。 |
| **kndctr_&lt;ORG_ID>_consent** | 15552000（180天） | 10-11字节 | 存储用户对网站的同意首选项。 |
| **kndctr_&lt;ORG_ID>_cluster** | 1800（30分钟） | 3-5字节 | 存储为当前Edge Network提供请求的请求区域。 URL路径中使用区域，以便Edge Network能够将请求路由到正确的区域。 如果用户使用不同的IP地址或以不同的会话连接，则请求将再次路由到最近的区域。 |
| **mbox** | 63072000（2年） | | 当Target迁移设置设置为true时存在。 它允许Web SDK设置Target [mbox Cookie](https://developer.adobe.com/target/implement/client-side/atjs/atjs-cookies/)。 |
| **mboxEdgeCluster** | 1800（30分钟） | | 当Target迁移设置设置为true时存在。 它允许Web SDK将正确的边缘群集传递给`at.js`，以便在用户浏览站点时，Target配置文件可以保持同步。 |
| **AMCV_###@AdobeOrg** | 34128000（395天） | | 启用[`idMigrationEnabled`](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/web-sdk/commands/configure/idmigrationenabled)时存在。 当站点的某些部分仍在使用`visitor.js`时，转换到Web SDK会很有帮助。 |

Edge Network使用`secure`和`sameSite="none"`属性设置所有Cookie。 如果您的网站上当前同时存在安全部分和不安全部分，则用户标识可能会不准确。 当用户从网站的安全区域导航到非安全区域时，Edge Network使用请求生成新的`ECID`。
