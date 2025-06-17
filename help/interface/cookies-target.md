---
description: 了解 [!DNL Adobe Target] 如何使用Cookie让网站运营者能够测试哪些在线内容和选件与访客更相关。
solution: Experience Cloud,Analytics,Target
title: Adobe Target Cookie
uuid: 44f7e32e-8d99-4682-8b54-8364d001b403
feature: Cookies
topic: Administration
role: Admin
level: Experienced
exl-id: c4399cc0-8333-47b8-b830-2ba7359f464a
source-git-commit: 95ca3a8e172166d7901873e0dc2e096e0bba7cd2
workflow-type: tm+mt
source-wordcount: '658'
ht-degree: 8%

---

# [!DNL Adobe Target] Cookie

[!DNL Adobe Target]使用Cookie让网站运营者能够测试哪些在线内容和选件与访客更相关。

>[!NOTE]
>
>本文中的信息仅适用于[[!DNL Target] at.js JavaScript库](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/targetglobalsettings.html){target=_blank}。
>
>有关在使用[[!DNL Adobe Experience Platform Web SDK]](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html){target=_blank}的[!DNL Target]实施中使用的Cookie的信息，请参阅“[!DNL Adobe Experience Platform Web SDK]是否使用Cookie？ 如果是这样，它使用哪些Cookie？” 在[DNL Platform Web SDK概述指南的常见问题解答中](https://experienceleague.adobe.com/docs/experience-platform/edge/web-sdk-faq.html){target=_blank}。
>
>如果需要，您可以更改本文中讨论的设置，但Cookie持续时间除外。 更改Cookie设置时，[请咨询您的客户代表](https://experienceleague.adobe.com/docs/target/using/cmp-resources-and-contact-information.html){target=_blank}。
>
>[!DNL Target]用户还可以创建自定义的第三方Cookie。

## 第一方Cookie

以下第一方Cookie存储在客户的域中：

| Cookie | 详细信息 |
| --- | --- |
| mbox | 存储有关访客的匿名标识符。<P>**Cookie域**：您提供mbox的域。 由于此Cookie来自您公司的域，因此Cookie是第一方Cookie。 示例： `mycompany.com`。 如果您的任何域名包括国家/地区代码（如`mycompany.co.uk`），请咨询客户服务部门来配置at.js以支持该代码。 有关自定义Cookie域的信息，如有必要，请参阅&#x200B;*[!DNL Adobe Target]开发人员指南*&#x200B;中[targetGlobalSettings](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/targetglobalsettings.html){target=_blank}下的“`cookieDomain`”。<P>**服务器域**： `clientcode.tt.omtrdc.net`，使用您[!DNL Target]帐户的客户端代码。<P>**Cookie持续时间**：自上次登录起，Cookie在访客的浏览器中保留两年。 无法更改 Cookie 持续时间。<P>Cookie会保留一些值以管理访客体验[!DNL Target]活动的方式：<P>**会话ID**：给定用户会话的唯一标识符。 默认情况下，会话在闲置 30 分钟后到期。如果您自己正在生成`sessionId`（例如，对于[服务器端实施](https://experienceleague.adobe.com/docs/target-dev/developer/server-side/server-side-overview.html){target=_blank}），请确保以下各项：<ul><li>会话ID可以是任何可打印的字符串，但空格、问号( ？ )、大括号( { } )或正斜杠( / )。</li><li>会话ID应为1至128个字符长。</li><li>对于特定会话，Cookie的值必须在多个请求中保持相同。</li><li>对于给定访客，在任何时间点都不应存在并行会话（不同的`sessionIds`）。</li></ul>使用会话ID路由到边缘群集中的特定节点。<ul><li>会话在服务器端活跃 30 分钟。因此，不应在用`tntId/thirdPartyId`提出上次请求后30分钟内对特定`tntId/thirdPartyId`使用不同的会话ID。 否则，对轮廓的更改可能会不一致且不可预测。</li><li>新会话ID必须在访客处于非活动状态30分钟后使用。</li><li>对多个`tntIds/thirdPartyIds`使用同一会话ID可能会导致由`tntId/thirdPartyIDs`标识的个人资料发生不可预测的更改。</li></ul>注意：请查看给定会话ID的并发请求数[限制](https://experienceleague.adobe.com/docs/target/using/troubleshoot/target-limits.html?lang=en#content-delivery){target=_blank}。<P>**pc ID**：访客浏览器的半永久ID。 持续存在，直到手动删除 Cookie 为止。<P>**check**：用于确定访客是否支持Cookie的简单测试值。 在每次访客请求页面时设置。<P>**禁用**：如果访客的加载时间超过了at.js文件中配置的超时值，则进行设置。 默认情况下，此超时持续一小时。 |
| at_check | 临时Cookie ，用于检查浏览器上是否启用了Cookie读/写功能。 |
| mboxEdgeCluster | 仅当[overrideMboxEdgeServer设置](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/targetglobalsettings.html){target=_blank}设置为`true`时，此Cookie才存在。 |

无法在这些第一方Cookie上使用HTTPOnly。 at.js JavaScript库需要读取/写入这些Cookie。 这些Cookie由at.js创建，不会从服务器进行设置。

可以使用at.js实施中的`secureOnly: true`配置在所有这些这些Cookie上启用`secure`设置。

## 第三方Cookie

以下第三方Cookie存储在`tt.omtrdc.net`上：

| Cookie | 详细信息 |
| --- | --- |
| customerclientcode！mboxPC | 如果启用了跨域，则存在此Cookie。 |
| customerclientcode！mboxSession | 如果启用了跨域，则存在此Cookie。 |

这些第三方Cookie是现成的，由[!DNL Target]边缘服务器设置。

可以在at.js实施中使用`secureOnly: true`配置在所有Cookie上启用`secure`设置。