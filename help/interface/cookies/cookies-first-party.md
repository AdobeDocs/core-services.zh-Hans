---
description: Analytics 使用 Cookie 来提供有关变量和组件的信息，这类信息无法在图像请求和浏览器会话之间永久保存。
keywords: cookies;隐私
seo-description: Analytics 使用 Cookie 来提供有关变量和组件的信息，这类信息无法在图像请求和浏览器会话之间永久保存。
seo-title: 第一方 Cookie
solution: Experience Cloud，Analytics
title: 第一方 Cookie
index: y
snippet: y
translation-type: tm+mt
source-git-commit: 2bdc4b7287ccacfc4d968278b2c3ffdaeddfc105

---


# 关于第一方cookie

Analytics 使用 Cookie 来提供有关变量和组件的信息，这类信息无法在图像请求和浏览器会话之间永久保存。这些无害的 Cookie 源自 Adobe 托管的域，称为第三方 Cookie。

许多浏览器和防间谍软件应用程序设计为拒绝和删除第三方cookie，包括Analytics数据收集中使用的cookie。为了规避浏览器和程序实施的跟踪限制，您可以实施第一方cookie。

可使用两个选项来实施第一方cookie

* Experience Platform ID服务。ID服务可使用JavaScript在第一方上下文中设置cookie。
* DNS条目。
* 如果您的站点使用该 `https:` 协议安全页面，并且您没有使用Experience Platform ID Service，则可以与Adobe合作获取一个SSL证书，以实施第一方Cookie

SSL证书颁发流程往往会令人困惑和费时。因此，Adobe与行业领先的认证中心(CA)建立了合作伙伴关系，并开发了一个集成流程，通过该流程购买和管理这些证书。

在您的允许下，我们将与我们的CA一起为您发布、部署和管理一个新的SHA-2SSL证书。Adobe将继续管理此证书，并确保意外过期、撤销或安全问题，这不会危及您组织的安全集合。

## Adobe 托管的证书计划

Adobe Managed Certificate Program是为第一方Cookie实施新的第三方SSL证书的推荐过程。

通过Adobe Managed Certificate程序，您无需额外费用即可为第一方Cookie实施一个新的第三方SSL证书。如果您目前拥有自己的客户托管SSL证书，请与Adobe客户关怀部门协商迁移到Adobe Managed Certificate Program。

### 实施

下面是如何为第一方Cookie实施新的第三方SSL证书：

1. 填写 [第一方cookie请求表](/help/interface/cookies/assets/FPC_Request_Form.xlsx) ，并通过客户关怀打开一个票证，请求在Adobe Managed计划上设置第一方Cookie。文档中利用示例说明了每个字段。

1. 创建CNAME记录(请参阅下面的说明)。收到票证后，CMS SSL专家应为您提供一对CNAME记录。必须在公司DNS服务器上配置这些记录，然后Adobe才能代表您购买证书。CNAME将类似于以下内容： **安全** -例如，主机名 `smetrics.example.com` 指向： `example.com.ssl.d1.omtrdc.net`。**非安全** -例如，主机名 `metrics.example.com` 指向： `example.com.d1.omtrdc.net`。

1. 这些CNAME就位后，Adobe将与DigicerT一起购买并安装Adobe生产服务器上的证书。如果您有现有的实施，应考虑使用访客迁移来维护现有访客。将证书实时推送到Adobe生产环境后，您可以将跟踪服务器变量更新为新的主机名。也就是说，如果站点不安全(https)，则更新该站点 `s.trackingServer`。如果站点为安全(https)，则更新和 `s.trackingServer``s.trackingServerSecure` 变量。

1. ping主机名(请参阅下面)。

1. 更新实施代码(见下文)。

### 维护和续订

SSL证书每年到期，这意味着Adobe必须每年为每个实施购买一个新证书。在每次实施接近期满时，组织内的所有受支持用户都将收到电子邮件通知。要使Adobe续订您的主机名，一个受支持的用户必须回复Adobe的电子邮件，并指示您计划继续使用过期的主机名进行数据收集。此时，Adobe会自动购买并安装新证书。

### 常见问题解答

| 问题 | 回答 |
|---|---|
| **此过程是否安全？** | 是的，Adobe Managed计划比我们原有的方法更加安全，因为证书或私钥不会在Adobe外部和颁发证书颁发机构的外部更改手。 |
| **Adobe如何为我们的域购买证书？** | 仅当您将指定的主机名(例如smetrics.example.com)指向Adobe拥有的主机名时，才能购买证书。这实质上是将此主机名委派给Adobe，并允许Adobe代表您购买证书。 |
| **我是否可以请求吊销证书？** | 是的，作为域所有者，您有权请求我们吊销证书。您只需与客户关怀部门打开一个票证，即可完成此操作。 |
| **此证书是否会使用SHA-2加密？** | 是，Adobe将与DigicerT一起颁发SHA-2证书。 |
| **这会产生任何额外费用吗？** | 不可以，Adobe没有额外费用向所有当前Analytics客户提供此服务。 |

## 创建CNAME记录

贵组织的网络操作团队应通过创建新的CNAME记录来配置DNS服务器。每个主机名都将数据转发至Adobe的数据收集服务器。

FPC专家为您提供配置的主机名以及要指向的CNAME。例如：

* **SSL主机名**：`smetrics.mysite.com`
* **SSL CNAME**：`mysite.com.ssl.d1.sc.omtrdc.net`
* **非SSL主机名**：`metrics.mysite.com`
* **非SSL CNAME**：`mysite.com.d1.sc.omtrdc.net`

只要实施代码未发生改变，此步骤就不会影响数据收集，并且可以在更新实施代码后随时完成。

>[!Nte：] Experience Cloud访客ID服务提供了一种配置CNAME以启用第一方Cookie的替代方法。

## ping主机名

ping主机名以确保正确转发。所有主机名都必须响应ping以防止数据丢失。

正确配置CNAME记录后，Adobe已确认安装证书，打开命令提示符并ping主机名。Using `mysite.com` as an example: `ping metrics.mysite.com`

如果一切均已成功设置，将返回与下面类似的信息：

```Pinging mysite.com.112.2o7.net [66.235.132.232] with 32 bytes of data:
Reply from 66.235.132.232: bytes=32 time=19ms TTL=246
Reply from 66.235.132.232: bytes=32 time=19ms TTL=246
Reply from 66.235.132.232: bytes=32 time=19ms TTL=246
Reply from 66.235.132.232: bytes=32 time=19ms TTL=246

Ping statistics for 66.235.132.232: Packets: Sent = 4, Received = 4, Lost = 0 (0% loss),
Approximate round trip times in milli-seconds: Minimum = 19ms, Maximum = 19ms, Average = 19ms
```

如果 CNAME 记录未正确设置或者未处于活动状态，将返回下列信息：

`Ping request could not find the host. Please check the name and try again.`

>[!Nte：] 如果您使用 `https:// protocol`，ping只会在FPC专家指定的上传日期后响应。此外，请务必ping安全主机名和非安全主机名，以确保在更新实施之前都能正确运行。

## 更新实施代码

在编辑网站上使用第一方Cookie的代码之前，请完成以下先决条件：

* 请求SSL证书，如Adobe Managed Certificate Program实施步骤中所述。
* 创建CNAME记录(请参阅上文)。
* ping主机名(请参阅上文)。

验证主机名对Adobe数据收集服务器进行响应和转发后，您可以更改实施以指向您自己的数据收集主机名。

1. Open your core JavaScript file (`s_code.js/AppMeasurement.js`).
1. 如果希望更新代码版本，请使用较新版本替换整个`s_code.js/AppMeasurement.js`   文件，然后替换所有插件或自定义设置（如果有）。**或者**，如果您要更新仅与第一方cookie相关的代码，请找到s. trackingServer和s. trackingServerSecure(如果使用SSL)变量，并将它们指向您的新数据集合主机名。Using mysite.com as an example:`s.trackingServer = "metrics.mysite.com"` `s.trackingServerSecure = "smetrics.mysite.com"`

1. 将更新后的核心JavaScript文件上传到您的站点。

1. 如果您从长期实施移至第一方cookie，或更改为其他第一方集合主机名，则建议将访客从先前域迁移到新域。

请参阅Analytics实施指南中的 [访客迁移](https://docs.adobe.com/help/en/analytics/implementation/javascript-implementation/visitor-migration.html) 。

上传JavaScript文件后，将所有内容配置为第一方cookie数据收集。我们建议您在接下来的几个小时监控Analytics报告，以确保数据收集照常继续。如果没有，请验证上述所有步骤已完成，并让您组织的一个受支持用户与客户服务部门联系。
