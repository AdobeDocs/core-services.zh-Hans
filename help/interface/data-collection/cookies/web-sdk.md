---
title: Adobe Experience Platform Web SDK Cookie
description: 了解Web SDK如何使用适用于您的实施的Cookie。
solution: Experience Cloud
feature: Cookies
topic: Administration
role: Admin
level: Experienced
source-git-commit: 66f78a04674a82335f5df20c4c15d983b6ebdc66
workflow-type: tm+mt
source-wordcount: '288'
ht-degree: 2%

---

# Adobe Experience Platform Web SDK Cookie

Adobe Experience Platform Web SDK使用Cookie来存储特定于您的实施的值。

| 名称 | 最大年龄 | 描述 |
|---|---|---|
| **kndct_orgid_identity** | 34128000（395天） | 存储ECID以及与ECID相关的其他信息。 |
| **kndctr_orgid_consent_check** | 7200（2小时） | 指示服务器查找同意首选项服务器端。 |
| **kndctr_orgid_consent** | 15552000（180天） | 存储用户对网站的同意首选项。 |
| **kndctr_orgid_cluster** | 1800（30 分钟） | 存储为当前Edge Network提供请求的请求区域。 URL路径中使用区域，以便Edge Network能够将请求路由到正确的区域。 如果用户使用不同的IP地址或以不同的会话连接，则请求将再次路由到最近的区域。 |
| **mbox** | 63072000（2年） | 当Target迁移设置设置为true时存在。 它允许Target [mbox Cookie](https://developer.adobe.com/target/implement/client-side/atjs/atjs-cookies/) 将由Web SDK设置。 |
| **mboxEdgeCluster** | 1800（30 分钟） | 当Target迁移设置设置为true时存在。 它允许Web SDK将正确的边缘群集传输到 `at.js` 这样，当用户跨站点导航时，Target配置文件可以保持同步。 |
| **AMCV_###@AdobeOrg** | 34128000（395天） | 前提条件 [`idMigrationEnabled`](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/commands/configure/idmigrationenabled) 已启用。 当站点的某些部分仍在使用时，在过渡到Web SDK时非常有用 `visitor.js`. |

Edge Network使用设置所有Cookie `secure` 和 `sameSite="none"` 属性。 如果您的网站上当前同时存在安全部分和不安全部分，则用户标识可能会不准确。 当用户从网站的安全区段导航到非安全区段时，Edge Network生成新的 `ECID` 请求。
