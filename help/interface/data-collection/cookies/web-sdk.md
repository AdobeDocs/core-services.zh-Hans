---
title: Adobe Experience Platform Web SDK Cookie
description: 了解Web SDK如何使用适用于您的实施的Cookie。
solution: Experience Cloud
feature: Cookies
topic: Administration
role: Admin
level: Experienced
exl-id: 14f06dc9-255e-4a6c-adec-471107cf202e
TQID: https://experienceleague.adobe.com/jysQ5m7o0cI3ECKz2RWZB4Kt3own7XAPm04pr4yLh-k
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
feature_v2:
  - id: fdbb8fc9-ffa3-4b86-88fe-aa4c5a3e1bc6
subfeature_v2:
  - id: b75843fa-0a67-4a44-a6b1-cc627b0481dc
  - id: fef08361-6ac5-460c-93fe-d063e40b6a49
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 0ce4fa63a4babc195f89c595009adcf19f34cdd9
workflow-type: tm+mt
source-wordcount: 396
ht-degree: 1%

---

# Adobe Experience Platform Web SDK Cookie

Adobe Experience Platform Web SDK使用Cookie来存储特定于您的实施的值。

| 名称 | 最大年龄 | 大小 | 描述 |
| ---| ---| ---| ---|
| **`AMCV_###@AdobeOrg`** | 34128000（395天） | 100-120字节（变量） | 启用[`idMigrationEnabled`](https://experienceleague.adobe.com/en/docs/experience-platform/collection/js/commands/configure/idmigrationenabled)时存在。 当站点的某些部分仍在使用`visitor.js`时，转换到Web SDK会很有帮助。 Web SDK在迁移期间会读取和写入此Cookie。 |
| **`demdex`** | 15552000（180天） | 不同 | 如果启用了Audience Manager ID同步，则会显示。 Audience Manager通过设置此Cookie来分配唯一ID，并支持ID同步、分段、建模和报表。 查看`demdex`Audience Manager Cookie[中的](audience-manager.md)。 |
| **`kndctr_<orgId>_identity`** | 34128000（395天） | 100-120字节（变量） | 存储该设备的ECID和其他相关信息。 |
| **`kndctr_<orgId>_cluster`** | 1800（30分钟） | 3-5字节 | 存储Edge Network区域（位置提示），用于提供当前用户的请求。 URL路径中使用区域，以便Edge Network能够将请求路由到正确的区域。 如果用户在Cookie生命周期内使用不同的IP地址连接，则请求将再次路由到最近的区域。 |
| **`kndctr_<orgId>_consent`** | 15552000（180天） | 10-11字节 | 存储访客的同意首选项。 无论是否同意，始终设置，因为它存储同意首选项本身。 |
| **`kndctr_<orgId>_consent_check`** | 7200（2小时） | | 会话范围的帮助程序，用于指示Edge Network在TTL过期后重新检查同意服务器端。 它会在缓存的同意后实施TTL。 |
| **`kndctr_<orgId>_personalization`** | 34128000（395天） | | 存储Adobe Target用于个性化内容的会话信息。 |
| **`mbox`** | 63072000（2年） | | 启用[`targetMigrationEnabled`](https://experienceleague.adobe.com/en/docs/experience-platform/collection/js/commands/configure/targetmigrationenabled)时存在。 它允许Web SDK设置Target [mbox Cookie](https://developer.adobe.com/target/implement/client-side/atjs/atjs-cookies/)。 |
| **`mboxEdgeCluster`** | 1800（30分钟） | | 启用[`targetMigrationEnabled`](https://experienceleague.adobe.com/en/docs/experience-platform/collection/js/commands/configure/targetmigrationenabled)时存在。 它允许Web SDK将正确的边缘群集传递给`at.js`，以便当用户跨站点导航时，Target配置文件可以保持同步。 |
| **`s_ecid`** | 63115200（2年） | ~45 字节 | 包含`s_ecid=MCMID\|<ECID>`格式的Experience Cloud ID (ECID/MID)副本。 作为ECID的第一方备份，主要用于CNAME（第一方）方案。 |

Edge Network使用`secure`和`sameSite="none"`属性设置所有Cookie。 如果您的网站上当前同时存在安全部分和不安全部分，则用户标识可能会不准确。 当用户从网站的安全区域导航到非安全区域时，Edge Network会使用请求生成新的`ECID`。
