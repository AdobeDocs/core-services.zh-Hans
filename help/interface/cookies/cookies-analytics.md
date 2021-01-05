---
description: 了解 Adobe Experience Cloud 中的 Adobe Analytics Cookie。
keywords: cookies;privacy
solution: Experience Cloud,Analytics,Target
title: '如何使用 Adobe Analytics Cookie '
uuid: e2d3d61d-2708-48b2-a7e6-2331f2aed8e0
translation-type: ht
source-git-commit: 3f26c1af19a0838913eec2b4135304f5f3fcf0b4
workflow-type: ht
source-wordcount: '757'
ht-degree: 100%

---


# Analytics Cookie{#analytics-cookies}

Adobe Analytics 使用 Cookie 区分来自不同浏览器的请求，并存储应用程序以后可以使用的有用信息。还可使用它们将浏览信息与客户记录相关联。

尤其是，Analytics 使用 Cookie 匿名定义新访客、帮助分析点击流数据并跟踪网站上的历史活动，如对特定营销活动的响应或销售周期的长度。

* [Cookie 名称：s_ecid](../cookies/cookies-mc.md#section-32fd753c3fa54452acd62b021434919a)
* [Cookie 名称：AMCV_###@AdobeOrg](../cookies/cookies-mc.md#section-a12aa2a9296940ae82d8921b381b8fb0)
* [Cookie 名称：s_cc](../cookies/cookies-analytics.md#section-03aa90aa7e36427b8cb12dc4a0f0291e)
* [Cookie 名称：s_cc](../cookies/cookies-analytics.md#section-03aa90aa7e36427b8cb12dc4a0f0291e)
* [Cookie 名称：s_sq](../cookies/cookies-analytics.md#section-8abfff3a302d494f81a3cfb91e3b09ff)
* [Cookie 名称：s_vi](../cookies/cookies-analytics.md#section-5d50a078de444d12b7d927d68ff3b679)
* [Cookie 名称：s_fid](../cookies/cookies-analytics.md#section-65e33f9bfc264959ac1513e2f4b10ac7)
* [插件设置的 Cookie](../cookies/cookies-analytics.md#section-a6b1cae8454945fab9eea5c7884c40fc)

Analytics 帮助中提供了有关[第一方 Cookie](/help/interface/cookies/cookies-first-party.md) 的更多信息。

## Cookie 名称：s_ecid {#section-32fd753c3fa54452acd62b021434919a}

| 属性 | 描述 |
|--- |--- |
| 存储的信息 | 包含 Experience Cloud ID (ECID) 或 MID 的副本。MID 存储在一个键值对中，它遵循以下语法：s_ecid=MCMID | `<ECID>` |
| 过期 | 2 年 |
| 使用情况 | 在客户端设置 AMCV Cookie 之后，此 Cookie 由客户的域设置。此 Cookie 的用途是允许在第一方状态中进行持久 ID 跟踪，并在 AMCV Cookie 过期时用作参考 ID。有关更多详细信息，请参阅此处的 AMCV Cookie。 |
| 位置 | 仅限 CNAME 客户。不适用于第三方场景。Cookie 存储在您的域中，该域与 CNAME 和 Analytics 图像请求使用的域相同。 |
| 大小 | 45 字节 |

## Cookie 名称：s_cc {#section-03aa90aa7e36427b8cb12dc4a0f0291e}

| 属性 | 描述 |
|--- |--- |
| 存储的信息 | 此 Cookie 通过 JavaScript 代码设置和读取，以确定是否已启用 Cookie（只需将其设置为“True”） |
| 过期 | 此 Cookie 是会话 Cookie，在浏览器关闭时过期 |
| 使用情况 | 所有帐户都只能使用一个 Cookie |
| 位置 | 此 Cookie 存储在页面的域中 |
| 大小 | 4 字节 |

## Cookie 名称：s_sq {#section-8abfff3a302d494f81a3cfb91e3b09ff}

| 属性 | 描述 |
|--- |--- |
| 存储的信息 | 当启用 ClickMap 功能或 Activity Map 功能时，此 Cookie 通过 JavaScript 代码设置和读取；它包含有关用户点击的上一个链接的信息 |
| 过期 | 此 Cookie 是会话 Cookie，在浏览器关闭时过期 |
| 使用情况 | 所有帐户都只能使用一个 Cookie |
| 位置 | 此 Cookie 存储在页面的域中 |
| 大小 | 根据页面 URL 大小而异，但通常为 100 - 200 字节 |

## Cookie 名称：s_vi {#section-5d50a078de444d12b7d927d68ff3b679}

| 属性 | 描述 |
|--- |--- |
| 存储的信息 | 独特访客 ID 时间戳/日期戳 |
| 过期 | 2 年 |
| 使用情况 | 此 Cookie 用于标识独特访客 |
| 位置 | 此 Cookie 存储在图像请求的域中 - 如果您使用的是第三方 Cookie，或您的域使用的是第一方 Cookie，则通常存储在 2o7.net 或 omtrdc.net 下客户特定的子域中。 |
| 大小 | 44 字节 |

>[!NOTE]
>
>每个 Analytics 访客 ID 均与 Adobe 服务器上的一个访客资料关联。访客资料在处于 1 年的非活动状态之后会被删除，这与任何访客 ID Cookie 过期日期无关。

## Cookie 名称：s_fid {#section-65e33f9bfc264959ac1513e2f4b10ac7}

| 属性 | 描述 |
|--- |--- |
| 存储的信息 | 备用独特访客 ID 时间戳/日期戳 |
| 过期 | 2 年 |
| 使用情况 | 如果标准 `s_vi` Cookie 由于受第三方 Cookie 限制而不可用，此 Cookie 可用于识别独特访客。不用于使用第一方 Cookie 的实施。 |
| 位置 | 此 Cookie 将作为第一方 Cookie 存储在您的域中。 |
| 大小 | 33 字节 |

## Cookie 标记

下表介绍了 Analytics Cookie 的标记：

| Cookie（设置方式） | httpOnly | Secure | SameSite |
|--- |--- |--- |--- |
| s_vi（http 响应） | 否 | 当 SameSite 为“无”且连接使用 HTTPS 时为“是” | 使用 CNAME 时，默认情况下为“Lax”。使用 2o7.net 或 omtrdc.net 时为“无”。 |
| s_ecid（http 响应） | 否 | 否 | &quot;Lax&quot; |
| s_fid (Javascript) | 否 | 否 | 未设置 |
| s_cc (Javascript) | 否 | 否 | 未设置 |
| s_sq (Javascript) | 否 | 否 | 未设置 |

>[!NOTE]
>
>如果使用单个 CNAME 跨多个域或属性进行跟踪，则应将 `s_vi` 的 SameSite 设置为“无”。要获取更改 Analytics Cookie 设置的帮助，请联系客户关怀。

## 插件设置的 Cookie {#section-a6b1cae8454945fab9eea5c7884c40fc}

可根据 Analytics 插件的使用情况来设置其他 Cookie。这些 Cookie 是代码片段，可供客户端在各种情况下使用。这些情况包括：从 URL 检索值；合并值以传递给 Analytics；捕获表单放弃，等等。有关每个插件所设置的 Cookie 的特定信息，请与 ClientCare 联系。例如，[!DNL s_vh]Set Once Per *和* Set and Get Last Value *插件使用* Cookie。

仅当电子邮件和浏览器共享相同的 Cookie 空间时，才能正确识别未使用 JavaScript 而传入图像请求的 Conversion 变量 (eVarX)，例如置入电子邮件内的代码。
