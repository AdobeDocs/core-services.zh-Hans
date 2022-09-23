---
description: 了解 Adobe Target 如何使用 Cookie，以便让网站运营者能够测试哪些在线内容和选件与访客更相关。
solution: Experience Cloud,Analytics,Target,Social
title: Adobe Target Cookie
feature: Cookies
topic: Administration
role: Administrator
level: Experienced
exl-id: c4399cc0-8333-47b8-b830-2ba7359f464a
source-git-commit: eb2ad8a8255915be47b6002a78cc810b522170d2
workflow-type: tm+mt
source-wordcount: '429'
ht-degree: 95%

---

# Adobe Target Cookie{#target-cookies}

Adobe Target 使用 Cookie 让网站运营者能够测试哪些在线内容和选件与访客更相关。

如果需要，可更改这些设置，但 Cookie 持续时间除外。更改 Cookie 设置时，请咨询您的客户代表。

>[!NOTE]
>
>Adobe Target 用户还可以创建自定义的第三方 Cookie。

| 设置 | 信息 |
| --- | --- |
| Cookie 名称 | mbox。 |
| Cookie 域 | 提供 mbox 的二级域和顶级域。由于这是来自您的公司域，所以此 Cookie 是第一方 Cookie。示例：`mycompany.com`。 |
| 服务器域 | `clientcode.tt.omtrdc.net`，使用您 [!DNL Adobe Target] 帐户的客户端代码。 |
| Cookie 持续时间 | 自访客上次登录起，Cookie 在访客的浏览器中保留两年。无法更改 Cookie 持续时间。 |



>[!NOTE]
>
>如果您的任何域名包括国家/地区代码（如 `mycompany.co.uk`），请咨询客户服务部门来配置您的 [!DNL at.js] 以支持此功能。

Cookie 会保留大量值以管理访客对 Adobe Target 促销活动的体验：

| 值 | 定义 |
| --- | --- |
| session ID | 给定用户会话的唯一标识符。默认情况下，会话在闲置 30 分钟后到期。如果您自己生成 sessionId（例如，用于服务器端实现），请确保以下各项：<ul><li>会话 ID 可以是任何可打印的字符串，但空格、问号 (? ) 或正斜杠 (/) 除外。</li><li>* 会话 ID 应为 1 至 128 个字符长。</li><li>对于特定会话，其值必须在多个请求间保持相同</li><li>对于给定访客，在任何时刻都不应存在同时进行的会话（不同的 sessionId）。</li></ul>使用会话 ID 路由到边缘群集中的特定节点。<ul><li>会话在服务器端活跃 30 分钟。因此，您不应将不同的会话ID用于特定 `tntId/thirdPartyId` 在使用 `tntId/thirdPartyId`. 否则，对个人资料的更改可能会不一致且不可预测。</li><li>对多个 `tntIds/thirdPartyIds` 使用同一会话 ID 可能会导致由 `tntId/thirdPartyIDs` 标识的个人资料产生不可预测的更改。</li></ul>**注意**：请查看给定会话 ID 的[并发请求数限制](https://experienceleague.adobe.com/docs/target/using/troubleshoot/target-limits.html?lang=en#content-delivery)。 |
| pc ID | 访客浏览器的半永久 ID。持续存在，直到手动删除 Cookie 为止。 |
| check | 用于确定访客是否支持 Cookie 的简单测试值。在每次访客请求页面时设置。 |
| disable | 如果访客的加载时间超出在 at.js 文件中配置的超时，则设置此项。默认情况下，此过程持续 1 小时。 |

