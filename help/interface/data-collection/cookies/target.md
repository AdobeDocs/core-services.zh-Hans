---
description: 了解 Adobe Target 如何使用 Cookie，以便让网站运营者能够测试哪些在线内容和选件与访客更相关。
solution: Target
title: Adobe Target Cookie
uuid: 44f7e32e-8d99-4682-8b54-8364d001b403
feature: Cookies
topic: Administration
role: Admin
level: Experienced
exl-id: c4399cc0-8333-47b8-b830-2ba7359f464a
source-git-commit: 9ee4d9b0e670dec35cda530892c49e36bf7cc107
workflow-type: tm+mt
source-wordcount: '627'
ht-degree: 17%

---

# Adobe Target Cookie

Adobe Target 使用 Cookie 让网站运营者能够测试哪些在线内容和选件与访客更相关。

>[!NOTE]
>
>本文中的信息仅适用于[Adobe Target JavaScript库](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/targetglobalsettings.html){target=_blank} (`at.js`)。 有关使用Web SDK实现Target的信息，请参阅[Adobe Experience Platform Web SDK Cookie](web-sdk.md)。
>
>如果需要，您可以更改本文中讨论的设置，但Cookie持续时间除外。 更改Cookie设置时，[请咨询您的帐户代表](https://experienceleague.adobe.com/docs/target/using/cmp-resources-and-contact-information.html){target=_blank}。

## 第一方Cookie

以下第一方Cookie存储在客户的域中：

| Cookie | 详细信息 |
| --- | --- |
| `mbox` | 存储有关访客的匿名标识符。<P>**Cookie域**：您提供mbox的域。 由于此Cookie来自您公司的域，因此Cookie是第一方Cookie。 如果您的任何域名包括国家/地区代码（如`example.co.uk`），请与客户服务部门合作配置`at.js`以支持此代码。 有关自定义Cookie域的信息，如有必要，请参阅Adobe Target开发人员指南中[targetGlobalSettings](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/targetglobalsettings.html){target=_blank}下的`cookieDomain`。<P>**服务器域**： `clientcode.tt.omtrdc.net`，使用Adobe Target帐户的客户端代码。<P>**Cookie持续时间**：自上次登录起，Cookie在访客的浏览器中保留两年。 无法更改 Cookie 持续时间。<P>Cookie会保留一些值以管理访客体验[!DNL Target]活动的方式：<P>**会话ID**：给定用户会话的唯一标识符。 默认情况下，会话在闲置 30 分钟后到期。如果您自己正在生成`sessionId`（例如，对于[服务器端实施](https://experienceleague.adobe.com/docs/target-dev/developer/server-side/server-side-overview.html){target=_blank}），请确保以下各项：<ul><li>会话ID可以是任何可打印的字符串，但空格、问号( ？ ) 或正斜杠 (/) 除外。</li><li>会话ID应为1至128个字符长。</li><li>对于特定会话，Cookie的值必须在多个请求中保持相同。</li><li>对于给定访客，在任何时间点都不应存在并行会话（不同的`sessionIds`）。</li></ul>使用会话ID路由到边缘群集中的特定节点。<ul><li>会话在服务器端活跃 30 分钟。因此，不应在用`tntId/thirdPartyId`提出上次请求后30分钟内对特定`tntId/thirdPartyId`使用不同的会话ID。 否则，对个人资料的更改可能会不一致且不可预测。</li><li>新会话ID必须在访客处于非活动状态30分钟后使用。</li><li>对多个`tntIds/thirdPartyIds`使用同一会话ID可能会导致由`tntId/thirdPartyIDs`标识的个人资料发生不可预测的更改。</li></ul>注意：请查看给定会话ID的并发请求数[限制](https://experienceleague.adobe.com/docs/target/using/troubleshoot/target-limits.html#content-delivery){target=_blank}。<P>**pc ID**：访客浏览器的半永久ID。 持续存在，直到手动删除 Cookie 为止。<P>**check**：用于确定访客是否支持Cookie的简单测试值。 在每次访客请求页面时设置。<P>**禁用**：如果访客的加载时间超过了at.js文件中配置的超时值，则进行设置。 默认情况下，此超时持续一小时。 |
| `at_check` | 临时Cookie ，用于检查浏览器上是否启用了Cookie读/写功能。 |
| `mboxEdgeCluster` | 仅当[overrideMboxEdgeServer设置](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/targetglobalsettings.html){target=_blank}设置为`true`时，此Cookie才存在。 |

无法在这些第一方Cookie上使用`HTTPOnly`。 `at.js` JavaScript库需要读取/写入这些Cookie。 这些Cookie由`at.js`创建，不是从服务器设置的。

可以使用`at.js`中的`secureOnly: true`配置在所有这些这些Cookie上启用`secure`设置。

## 第三方Cookie

Adobe Target用户可以创建自定义的第三方Cookie。 以下第三方Cookie存储在`tt.omtrdc.net`上：

| Cookie | 详细信息 |
| --- | --- |
| `customerclientcode!mboxPC` | 如果启用了跨域，则存在。 |
| `customerclientcode!mboxSession` | 如果启用了跨域，则存在。 |

这些第三方Cookie是开箱即用的，由Adobe Target数据收集服务器设置。

可以使用`at.js`中的`secureOnly: true`配置在所有Cookie上启用`secure`设置。
