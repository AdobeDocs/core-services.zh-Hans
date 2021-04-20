---
description: 了解 Adobe Target 如何使用 Cookie，以便让网站运营者能够测试哪些在线内容和选件与访客更相关。
keywords: cookies;隐私
solution: Experience Cloud,Analytics,Target,Social
title: 'Adobe Target Cookie '
uuid: 44f7e32e-8d99-4682-8b54-8364d001b403
feature: Cookies
topic: Administration
role: Administrator
level: Experienced
exl-id: c4399cc0-8333-47b8-b830-2ba7359f464a
translation-type: tm+mt
source-git-commit: dcb6fa5d8458995cba66bc2f89c954aa6bcd5923
workflow-type: tm+mt
source-wordcount: '410'
ht-degree: 55%

---

# Adobe Target Cookie{#target-cookies}

Adobe Target 使用 Cookie 让网站运营者能够测试哪些在线内容和选件与访客更相关。

您可以根据需要更改这些设置，但Cookie持续时间除外。 更改 Cookie 设置时，请咨询您的客户代表。

>[!NOTE]
>
>Adobe Target 用户还可以创建自定义的第三方 Cookie。

| 设置 | 信息 |
| --- | --- |
| Cookie 名称 | mbox。 |
| Cookie 域 | 提供 mbox 的二级域和顶级域。由于这是来自您的公司域，所以此 Cookie 是第一方 Cookie。示例：`mycompany.com`。 |
| Server domain | `clientcode.tt.omtrdc.net`[!DNL Adobe Target]，使用您帐户的客户代码。 |
| Cookie 持续时间 | 自访客上次登录起，Cookie 在访客的浏览器中保留两年。无法更改 Cookie 持续时间。 |



>[!NOTE]
>
>如果您的任何域名包括国家/地区代码（如 `mycompany.co.uk`），请咨询客户服务部门来配置您的 [!DNL at.js] 以支持此功能。

Cookie 会保留大量值以管理访客对 Adobe Target 促销活动的体验：

| 值 | 定义 |
| --- | --- |
| session ID | 给定用户会话的唯一标识符。 默认情况下，会话在30分钟不活动后过期。 如果您是自己生成sessionId（例如，针对服务器端实现），请确保：<ul><li>会话ID可以是除空格、问号(? )或正斜杠(/)。</li><li>*会话ID的长度应介于1到128个字符之间。</li><li>对于特定会话，其值必须在多个请求中保持相同</li><li>在任何时间点，您都不应具有给定访客的并行会话（不同的sessionId）。</li></ul>使用会话ID路由到边缘群集中的特定节点。<ul><li>在服务器端，会话处于活动状态30分钟。 因此，在使用`tntId/thirdPartyId`发出的最后一个请求后30分钟内，不应对特定`tntId/thirdPartyId`使用其他会话ID。 否则，对用户档案的更改可能不一致且不可预测。</li><li>对多个`tntIds/thirdPartyIds`使用同一会话ID可能会对由`tntId/thirdPartyIDs`标识的用户档案造成不可预知的更改。</li></ul> |
| pc ID | 访客浏览器的半永久 ID。持续存在，直到手动删除 Cookie 为止。 |
| check | 用于确定访客是否支持 Cookie 的简单测试值。在每次访客请求页面时设置。 |
| disable | 设置访客的加载时间是否超过在at.js文件中配置的超时。 默认情况下，该设置持续 1 小时。 |

