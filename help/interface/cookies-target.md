---
description: 了解 Adobe Target 如何使用 Cookie，以便让网站运营者能够测试哪些在线内容和选件与访客更相关。
solution: Experience Cloud,Analytics,Target
title: Adobe Target Cookie
uuid: 44f7e32e-8d99-4682-8b54-8364d001b403
feature: Cookies
topic: Administration
role: Admin
level: Experienced
exl-id: c4399cc0-8333-47b8-b830-2ba7359f464a
source-git-commit: a1d24f95b1ac567686d58af8adf0132e5beb8f2a
workflow-type: tm+mt
source-wordcount: '688'
ht-degree: 23%

---

# Adobe Target Cookie

[!DNL Adobe Target] 使用 Cookie 让网站运营者能够测试哪些在线内容和选件与访客更相关。

>[!NOTE]
>
>本文中的信息适用于 [[!DNL Target] at.js JavaScript库](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/targetglobalsettings.html?lang=zh-Hans){target=_blank} 仅此而已。
>
>有关a中使用的Cookie的信息 [!DNL Target] 使用实施 [[!DNL Adobe Experience Platform Web SDK]](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=zh-Hans){target=_blank}, see "Does the [!DNL Adobe Experience Platform Web SDK] use cookies? If so, what cookies does it use?" in [Frequently Asked questions in the DNL Platform Web SDK overview guide](https://experienceleague.adobe.com/docs/experience-platform/edge/web-sdk-faq.html){target=_blank}.
>
>如果需要，您可以更改本文中讨论的设置，但Cookie持续时间除外。 [更改 Cookie 设置时，请咨询您的客户代表。](https://experienceleague.adobe.com/docs/target/using/cmp-resources-and-contact-information.html){target=_blank}
>
>[!DNL Target] 用户还可以创建自定义的第三方 Cookie。

## 第一方 Cookie

以下第一方Cookie存储在客户的域中：

| Cookie | 详细信息 |
| --- | --- |
| mbox | 存储有关访客的匿名标识符。<P>**Cookie域**：您从中提供mbox的域。 由于此Cookie来自您公司的域，因此Cookie是第一方Cookie。 示例: `mycompany.com`. 如果您的任何域名包括国家/地区代码，例如 `mycompany.co.uk`，请与您的客户服务部门合作来配置at.js以支持此代码。 有关自定义Cookie域的信息（如有必要），请参阅“`cookieDomain`“，在 [targetGlobalSettings](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/targetglobalsettings.html?lang=zh-Hans){target=_blank} 在 *[!DNL Adobe Target]开发人员指南*.<P>**服务器域**： `clientcode.tt.omtrdc.net`，使用您的客户端代码 [!DNL Target] 帐户。<P>**Cookie持续时间**：自上次登录起，Cookie在访客的浏览器中保留两年。 无法更改 Cookie 持续时间。<P>Cookie会保留一些值以管理访客的体验 [!DNL Target] 活动：<P>**会话ID**：给定用户会话的唯一标识符。 默认情况下，会话在闲置 30 分钟后到期。如果您正在生成 `sessionId` 您自己(例如， [服务器端实施](https://experienceleague.adobe.com/docs/target-dev/developer/server-side/server-side-overview.html){target=_blank})，确保以下各项：<ul><li>会话ID可以是任何可打印的字符串，但空格、问号( ？ ) 或正斜杠 (/) 除外。</li><li>会话ID的长度应为1到128个字符。</li><li>对于特定会话，Cookie的值必须在多个请求中保持相同。</li><li>绝不应该有并行会话(不同的 `sessionIds`)。</li></ul>使用会话ID路由到边缘群集中的特定节点。<ul><li>会话在服务器端活跃 30 分钟。因此，您不应为特定使用不同的会话ID `tntId/thirdPartyId` 在用发出上一个请求后的30分钟内 `tntId/thirdPartyId`. 否则，对个人资料的更改可能会不一致且不可预测。</li><li>新会话ID必须在访客处于非活动状态三十分钟后使用。</li><li>在多个会话ID中使用 `tntIds/thirdPartyIds` 可能会导致由标识的配置文件发生不可预测的更改 `tntId/thirdPartyIDs`.</li></ul>注意：请参阅 [并发请求数量的限制](https://experienceleague.adobe.com/docs/target/using/troubleshoot/target-limits.html?lang=en#content-delivery){target=_blank} 获取给定的会话ID。<P>**pc ID**：访客浏览器的半永久ID。 持续存在，直到手动删除 Cookie 为止。<P>**check**：用于确定访客是否支持Cookie的简单测试值。 在每次访客请求页面时设置。<P>**disable**：如果访客的加载时间超过了at.js文件中配置的超时值，则进行设置。 默认情况下，此超时持续一小时。 |
| at_check | 临时Cookie ，检查浏览器上是否启用了Cookie读/写功能。 |
| mboxEdgeCluster | 此Cookie仅存在于 [overrideMboxEdgeServer设置](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/targetglobalsettings.html?lang=zh-Hans){target=_blank} 设置为 `true`. |

无法对这些第一方Cookie使用HTTPOnly。 at.js JavaScript库需要读取/写入这些Cookie。 这些Cookie由at.js创建，不会从服务器进行设置。

此 `secure` 可以使用在所有这些Cookie上启用设置 `secureOnly: true` at.js实施中的配置。

## 第三方 Cookie

以下第三方Cookie存储在上 `tt.omtrdc.net`：

| Cookie | 详细信息 |
| --- | --- |
| customerclientcode！mboxPC | 如果启用了跨域，则存在此Cookie。 |
| customerclientcode！mboxSession | 如果启用了跨域，则存在此Cookie。 |

这些第三方Cookie是开箱即用的，由 [!DNL Target] 边缘服务器。

此 `secure` 可以使用在所有Cookie上启用设置 `secureOnly: true` at.js实施中的配置。