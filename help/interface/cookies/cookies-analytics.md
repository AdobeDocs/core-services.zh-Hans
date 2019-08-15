---
description: Adobe Analytics 使用 Cookie 区分来自不同浏览器的请求，并存储应用程序将来可使用的有用信息。这些 Cookie 还可以用来将浏览信息与客户记录相关联。
keywords: cookies;隐私
seo-description: Adobe Analytics 使用 Cookie 区分来自不同浏览器的请求，并存储应用程序将来可使用的有用信息。这些 Cookie 还可以用来将浏览信息与客户记录相关联。
seo-title: Analytics Cookie
solution: Marketing Cloud,Analytics,Target,Social
title: Analytics Cookie
uuid: e2d3d61d-2708-48b2-a7e6-2331f2aed8e0
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: f59badcd3423ada51a3fe0c605158a009d5b1d64

---


# Analytics Cookie{#analytics-cookies}

Adobe Analytics 使用 Cookie 区分来自不同浏览器的请求，并存储应用程序将来可使用的有用信息。这些 Cookie 还可以用来将浏览信息与客户记录相关联。

具体来说，Analytics 可通过 Cookie 以匿名方式定义新访客、协助分析点击流数据，并跟踪网站上的历史活动，如针对特定促销活动的响应或销售周期的长度。

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
| 存储的信息 | 包含 Experience Cloud ID (ECID) 或 MID 的副本。MID存储在遵循this语法的密钥值对中，s_ ecid= MCMID | <ECID> |
| 过期 | 2 年 |
| 使用情况 | 在客户端设置 AMCV Cookie 之后，此 Cookie 由客户的域设置。此 Cookie 的用途是允许在第一方状态中进行持久 ID 跟踪，并在 AMCV Cookie 过期时用作参考 ID。有关更多详细信息，请参阅此处的 AMCV Cookie。 |
| 位置 | 仅限 CNAME 客户。不适用于第三方场景。Cookie 存储在您的域中，该域与 CNAME 和 Analytics 图像请求使用的域相同。 |
| 大小 | 45 字节 |

## Cookie 名称：s_cc {#section-03aa90aa7e36427b8cb12dc4a0f0291e}

| 属性 | 描述 |
|--- |--- |
| 存储的信息 | 该 Cookie 通过 JavaScript 代码设置和读取，用于确定是否启用了 Cookie（只需设为“True”） |
| 过期 | 此 Cookie 是会话 Cookie，关闭浏览器之后即到期 |
| 使用情况 | 所有帐户只有一个 Cookie |
| 位置 | 此 Cookie 存储在页面的域中 |
| 大小 | 4 字节 |

## Cookie 名称：s_sq {#section-8abfff3a302d494f81a3cfb91e3b09ff}

| 属性 | 描述 |
|--- |--- |
| 存储的信息 | 在启用 ClickMap 功能和 Activity Map 功能后，将通过 JavaScript 代码设置并读取该 Cookie；它包含用户上一次点击的链接的相关信息 |
| 过期 | 此 Cookie 是会话 Cookie，关闭浏览器之后即到期 |
| 使用情况 | 所有帐户只有一个 Cookie |
| 位置 | 此 Cookie 存储在页面的域中 |
| 大小 | 根据页面URL大小而异，但通常为100-200字节 |

## Cookie 名称：s_vi {#section-5d50a078de444d12b7d927d68ff3b679}

| 属性 | 描述 |
|--- |--- |
| 存储的信息 | 独特访客 ID 时间/日期戳记 |
| 过期 | 2 年 |
| 使用情况 | 此 Cookie 用于识别独特访客 |
| 位置 | 此 Cookie 存储在图像请求的域（如果您使用的是第三方 Cookie，通常为 2O7.net）或您的域（如果您使用的是第一方 Cookie）中。 |
| 大小 | 44 字节 |

>[!NOTE]
>
>每个 Analytics 访客 ID 均与 Adobe 服务器上的一个访客资料关联。访客资料在处于 1 年的非活动状态之后会被删除，这与任何访客 ID Cookie 过期日期无关。

## Cookie 名称：s_fid {#section-65e33f9bfc264959ac1513e2f4b10ac7}

| 属性 | 描述 |
|--- |--- |
| 存储的信息 | 回退独特访客 ID 时间戳/日期戳 |
| 过期 | 5 年 |
| 使用情况 | 如果由于受第三方 Cookie 限制标准的 s_vi Cookie 不可用，将使用此 Cookie 来识别独特访客。在使用第一方 Cookie 的实施中不会使用此 Cookie。 |
| 位置 | 此 Cookie 作为第一方 Cookie 存储在您的域中。 |
| 大小 | 33 字节 |

## 插件设置的 Cookie {#section-a6b1cae8454945fab9eea5c7884c40fc}

其他 Cookie 可根据 Analytics 插件的使用情况来设置。这些 Cookie 是提供给客户端的代码段，可用在各种环境中。这些环境包括：从 URL 检索值、连接要传递到 Analytics 的值、捕获表单放弃等。有关每个插件所设置的 Cookie 的特定信息，请与 ClientCare 联系。例如，[!DNL s_vh]Set Once Per *和* Set and Get Last Value *插件使用* Cookie。

仅当电子邮件和浏览器共享相同的 Cookie 空间时，才能正确识别未使用 JavaScript 而传入图像请求的 Conversion 变量 (eVarX)，例如置入电子邮件内的代码。
