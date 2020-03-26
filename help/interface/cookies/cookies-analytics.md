---
description: Adobe Analytics使用cookie区分来自不同浏览器的请求，并存储应用程序稍后可使用的有用信息。 它们还可用于将浏览信息与客户记录相关联。
keywords: cookies;privacy
seo-description: Adobe Analytics使用cookie区分来自不同浏览器的请求，并存储应用程序稍后可使用的有用信息。 它们还可用于将浏览信息与客户记录相关联。
seo-title: Analytics Cookie
solution: Marketing Cloud,Analytics,Adobe Target,Adobe Social
title: Analytics Cookie
uuid: e2d3d61d-2708-48b2-a7e6-2331f2aed8e0
translation-type: tm+mt
source-git-commit: f7ec8bf6087a18be41c9efbf05f60e6cfd24e566

---


# Analytics Cookie{#analytics-cookies}

Adobe Analytics使用cookie区分来自不同浏览器的请求，并存储应用程序稍后可使用的有用信息。 它们还可用于将浏览信息与客户记录相关联。

特别是，Analytics使用cookies匿名定义新访客，帮助分析点击流数据，并跟踪网站上的历史活动，如对特定活动的响应或销售周期的长度。

* [Cookie 名称：s_ecid](../cookies/cookies-mc.md#section-32fd753c3fa54452acd62b021434919a)
* [Cookie 名称：AMCV_###@AdobeOrg](../cookies/cookies-mc.md#section-a12aa2a9296940ae82d8921b381b8fb0)
* [Cookie 名称：s_cc](../cookies/cookies-analytics.md#section-03aa90aa7e36427b8cb12dc4a0f0291e)
* [Cookie 名称：s_cc](../cookies/cookies-analytics.md#section-03aa90aa7e36427b8cb12dc4a0f0291e)
* [Cookie 名称：s_sq](../cookies/cookies-analytics.md#section-8abfff3a302d494f81a3cfb91e3b09ff)
* [Cookie 名称：s_vi](../cookies/cookies-analytics.md#section-5d50a078de444d12b7d927d68ff3b679)
* [Cookie 名称：s_fid](../cookies/cookies-analytics.md#section-65e33f9bfc264959ac1513e2f4b10ac7)
* [插件设置的 Cookie](../cookies/cookies-analytics.md#section-a6b1cae8454945fab9eea5c7884c40fc)

有关第一方Cookie的Analytics帮助， [请参阅更多信息](/help/interface/cookies/cookies-first-party.md)。

## Cookie 名称：s_ecid {#section-32fd753c3fa54452acd62b021434919a}

| 属性 | 描述 |
|--- |--- |
| 存储的信息 | 包含 Experience Cloud ID (ECID) 或 MID 的副本。MID 存储在一个键值对中，它遵循以下语法：s_ecid=MCMID | `<ECID>` |
| 过期 | 2年 |
| 使用情况 | 在客户端设置 AMCV Cookie 之后，此 Cookie 由客户的域设置。此 Cookie 的用途是允许在第一方状态中进行持久 ID 跟踪，并在 AMCV Cookie 过期时用作参考 ID。有关更多详细信息，请参阅此处的 AMCV Cookie。 |
| 位置 | 仅限 CNAME 客户。不适用于第三方场景。Cookie 存储在您的域中，该域与 CNAME 和 Analytics 图像请求使用的域相同。 |
| 大小 | 45 字节 |

## Cookie 名称：s_cc {#section-03aa90aa7e36427b8cb12dc4a0f0291e}

| 属性 | 描述 |
|--- |--- |
| 存储的信息 | 此Cookie由JavaScript代码设置和读取，以确定是否启用Cookie（只需设置为“True”） |
| 过期 | 此Cookie是会话Cookie，在浏览器关闭时过期 |
| 使用情况 | 所有帐户只能使用一个Cookie |
| 位置 | 此Cookie存储在页面的域中 |
| 大小 | 4 字节 |

## Cookie 名称：s_sq {#section-8abfff3a302d494f81a3cfb91e3b09ff}

| 属性 | 描述 |
|--- |--- |
| 存储的信息 | 当启用ClickMap功能或活动图功能时，JavaScript代码会设置和读取此Cookie;它包含用户单击的上一个链接的相关信息 |
| 过期 | 此Cookie是会话Cookie，在浏览器关闭时过期 |
| 使用情况 | 所有帐户只能使用一个Cookie |
| 位置 | 此Cookie存储在页面的域中 |
| 大小 | 根据页面 URL 大小而异，但通常为 100 - 200 字节 |

## Cookie 名称：s_vi {#section-5d50a078de444d12b7d927d68ff3b679}

| 属性 | 描述 |
|--- |--- |
| 存储的信息 | 独特访客 ID 时间戳/日期戳 |
| 过期 | 2年 |
| 使用情况 | 此Cookie用于标识唯一访客 |
| 位置 | 此Cookie存储在图像请求的域中——通常是客户特定的子域，如果您使用的是第三方Cookie，或者您的域使用的是第一方Cookie，则位于2o7.net或omtrdc.net下。 |
| 大小 | 44 字节 |

>[!NOTE]
>
>每个 Analytics 访客 ID 均与 Adobe 服务器上的一个访客资料关联。访客资料在处于 1 年的非活动状态之后会被删除，这与任何访客 ID Cookie 过期日期无关。

## Cookie 名称：s_fid {#section-65e33f9bfc264959ac1513e2f4b10ac7}

| 属性 | 描述 |
|--- |--- |
| 存储的信息 | 回退唯一访客ID时间／日期戳 |
| 过期 | 2年 |
| 使用情况 | This cookie is used to identify a unique visitor if the standard  `s_vi` cookie is unavailable due to third-party cookie restrictions. 不用于使用第一方Cookie的实施。 |
| 位置 | 此Cookie作为第一方Cookie存储在您的域中。 |
| 大小 | 33 字节 |

## Cookie标记

下表介绍了Analytics cookies的标记：

| Cookie（设置方式） | httpOnly | Secure | SameSite |
|--- |--- |--- |--- |
| s_vi（http响应） | 否 | 当SameSite为“无”且连接使用HTTPS时为“是” | 默认情况下，使用CNAME时为“lax”。 使用2o7.net或omtrdc.net时为“无”。 |
| s_ecid（http响应） | 否 | 否 | &quot;Lax&quot; |
| s_fid(Javascript) | 否 | 否 | 取消设置 |
| s_cc(Javascript) | 否 | 否 | 取消设置 |
| s_sq(Javascript) | 否 | 否 | 取消设置 |

>[!NOTE] 如果使用单个CNAME跨多个域或属性进行跟踪，则SameSite应设置为“无” `s_vi`。 要获得更改Analytics Cookie设置的帮助，请与客户服务联系。

## 插件设置的 Cookie {#section-a6b1cae8454945fab9eea5c7884c40fc}

可以根据Analytics插件的使用设置其他Cookie。 这些Cookie是可供客户在各种情况下使用的代码片段。 这些情况包括：从URL检索值；连接要传递到Analytics的值；捕获表单放弃等。 有关每个插件所设置的 Cookie 的特定信息，请与 ClientCare 联系。例如，[!DNL s_vh]Set Once Per *和* Set and Get Last Value *插件使用* Cookie。

仅当电子邮件和浏览器共享相同的 Cookie 空间时，才能正确识别未使用 JavaScript 而传入图像请求的 Conversion 变量 (eVarX)，例如置入电子邮件内的代码。
