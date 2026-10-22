---
title: Adobe Experience Platform Web SDK Cookie
description: 了解Web SDK如何使用适用于您的实施的Cookie。
solution: Experience Cloud
feature: Cookies
topic: Administration
role: Admin
level: Experienced
exl-id: 14f06dc9-255e-4a6c-adec-471107cf202e
TQID: 'https://experienceleague.adobe.com/jysQ5m7o0cI3ECKz2RWZB4Kt3own7XAPm04pr4yLh-k'
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
    internal-label: CX Enterprise
feature_v2:
  - id: fdbb8fc9-ffa3-4b86-88fe-aa4c5a3e1bc6
    internal-label: Administration
subfeature_v2:
  - id: b75843fa-0a67-4a44-a6b1-cc627b0481dc
    internal-label: Support
  - id: fef08361-6ac5-460c-93fe-d063e40b6a49
    internal-label: Getting started
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: d378ca77-2da1-4f39-ad92-1917fe974a38
    internal-label: Experienced
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: 7b12d5debfccd62ab7b416e9a6fe278d251a4ca5
workflow-type: tm+mt
source-wordcount: '984'
ht-degree: 0%
---
# Adobe Experience Platform Web SDK Cookie

Adobe Experience Platform Web SDK使用Cookie来存储特定于您的实施的值。

| 名称 | 最大年龄 | 大小 | 描述 |
| --- | --- | --- | --- |
| **`AMCV_###@AdobeOrg`** | 33696000（390天）当由网络SDK编写时 | 由Web SDK (`MCMID\|<ECID>`)写入时为44字节；由`VisitorAPI.js`写入时较大 | 在启用[`idMigrationEnabled`](https://experienceleague.adobe.com/en/docs/experience-platform/collection/js/commands/configure/idmigrationenabled)时存在，这是默认设置。 当站点的某些部分仍在使用`VisitorAPI.js`时，转换到Web SDK会很有帮助。 Web SDK会读取此Cookie以重用现有的ECID。 Edge Network返回ECID后，如果该Cookie缺失或包含其他ECID，则Web SDK会将其写入此Cookie。 |
| **`com.adobe.alloy.getTld`** | 无（会话Cookie，立即删除） | 22字节 | Web SDK在内部使用的临时帮助程序Cookie，用于确定当前站点的顶级域。 Web SDK在加载库时、运行`configure`命令之前以及评估同意之前写入和删除此Cookie，以便Cookie扫描程序可以在同意之前报告其设置。 Cookie仅包含其自身的名称，不会存储行为或配置文件数据。 |
| **`demdex`** | 15552000（180天） | 不同 | `demdex.net`域上的第三方Cookie。 在启用[`thirdPartyCookiesEnabled`](https://experienceleague.adobe.com/en/docs/experience-platform/collection/js/commands/configure/thirdpartycookiesenabled)（默认）并且浏览器默认允许第三方Cookie（如Chrome或Edge）时存在。 在这种情况下，Web SDK将身份请求发送给`adobedc.demdex.net`，后者会设置此Cookie。 Audience Manager使用此Cookie分配唯一ID并支持ID同步、分段、建模和报表。 查看[Audience Manager Cookie](audience-manager.md)中的`demdex`。 |
| **`kndctr_<orgId>_identity`** | 34128000（395天） | 100-120字节（变量） | 存储该设备的ECID和其他相关信息。 |
| **`kndctr_<orgId>_cluster`** | 1800（30分钟） | 3-5字节 | 存储Edge Network区域（位置提示），用于提供当前用户的请求。 URL路径中使用区域，以便Edge Network能够将请求路由到正确的区域。 如果用户在Cookie生命周期内使用不同的IP地址连接，则请求将再次路由到最近的区域。 |
| **`kndctr_<orgId>_consent`** | 15552000（180天） | 10-11字节 | 存储访客的同意首选项。 无论是否同意，始终设置，因为它存储同意首选项本身。 |
| **`kndctr_<orgId>_consent_check`** | 7200（2小时） | | 会话范围的帮助程序，用于指示Edge Network在TTL过期后重新检查同意服务器端。 它会在缓存的同意后实施TTL。 |
| **`kndctr_<orgId>_personalization`** | 34128000（395天） | | 存储Adobe Target用于个性化内容的会话信息。 |
| **`kndctr_<orgId>_advertising`** | 31622400（366天），每次更新Cookie时都会续订 | 80字节到1 KB（变量） | 当Adobe Advertising组件（测试版）包含在您的Web SDK内部版本中并且访客的同意为`in`时存在。 当页面URL包含Adobe Advertising点击参数（`s_kwcid`或`ef_id`），或配置了[Adobe Advertising DSP](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/configure/advertising)广告商时，Web SDK将写入此Cookie。 它存储URL编码的JSON，该JSON可以包括搜索点击数据(`_les_lsc`)、经过哈希处理的IP地址、LiveRamp RampID信封（在配置了RampID JavaScript路径时）以及用于限制重复转换的转换时间戳。 在默认允许第三方Cookie的浏览器中，它还会存储Adobe Advertising浏览者ID并显示点击数据(`ev_lcc`)。 此Cookie仅在当前主机名上设置。 该组件还从`pixel.everesttech.net`、`www.everestjs.net`（当配置了ID5合作伙伴ID时）和您的RampID `ats.js`路径加载资源。 这些资源可以设置自己的Cookie，但这不会列在此页面上。 |
| **`kndctr_<orgId>_bc_session_id`** | 无（会话Cookie） | | 在使用Brand Concierge组件（测试版）时存在。 存储Brand Concierge聊天会话ID。 Web SDK仅在启用[`stickyConversationSession`](https://experienceleague.adobe.com/en/docs/experience-platform/collection/js/commands/configure/conversation)时才读取此Cookie，以便聊天会话在页面加载之间持续存在。 |
| **`mbox`** | 63072000（2年） | | 启用[`targetMigrationEnabled`](https://experienceleague.adobe.com/en/docs/experience-platform/collection/js/commands/configure/targetmigrationenabled)时存在。 它允许Web SDK设置Target [mbox Cookie](https://developer.adobe.com/target/implement/client-side/atjs/atjs-cookies/)。 |
| **`mboxEdgeCluster`** | 1800（30分钟） | | 启用[`targetMigrationEnabled`](https://experienceleague.adobe.com/en/docs/experience-platform/collection/js/commands/configure/targetmigrationenabled)时存在。 它允许Web SDK将正确的边缘群集传递给`at.js`，以便当用户跨站点导航时，Target配置文件可以保持同步。 当`kndctr_<orgId>_cluster` Cookie不存在时，Web SDK还会读取此Cookie以将请求路由到匹配的Edge Network区域。 |
| **`s_ecid`** | 63115200（2年） | ~45 字节 | 包含`s_ecid=MCMID\|<ECID>`格式的CX Enterprise ID (ECID/MID)副本。 作为ECID的第一方备份，主要用于CNAME（第一方）方案。 启用[`idMigrationEnabled`](https://experienceleague.adobe.com/en/docs/experience-platform/collection/js/commands/configure/idmigrationenabled)后，Web SDK会读取此Cookie以重用现有的ECID。 |
| **Audience Manager Cookie目标**（名称不同） | 864000（10天），除非目标指定了不同的生命周期 | 不同 | 当Edge Network返回访客的Audience Manager [Cookie目标](https://experienceleague.adobe.com/en/docs/audience-manager/user-guide/features/destinations/custom-destinations/create-cookie-destination)时存在。 Web SDK使用目标中定义的Cookie名称、值和域来写入第一方Cookie。 值采用URL编码，与Audience Manager Data Integration Library (DIL)一致。 |

Edge Network使用`secure`和`sameSite="none"`属性设置其所有Cookie。 如果您的网站上当前同时存在安全部分和不安全部分，则用户标识可能会不准确。 当用户从网站的安全区域导航到非安全区域时，Edge Network会使用请求生成新的`ECID`。

Web SDK自行创建的Cookie而不是在Edge Network的方向上创建的Cookie使用不同的属性。 `AMCV_###@AdobeOrg` Cookie和Audience Manager Cookie目标仅在HTTPS页面上包含`secure`和`sameSite="none"`属性。 `com.adobe.alloy.getTld`和`kndctr_<orgId>_advertising` Cookie使用浏览器的默认属性。
