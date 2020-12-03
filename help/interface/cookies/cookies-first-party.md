---
description: Analytics 使用 Cookie 来提供有关变量和组件的信息，这类信息无法在图像请求和浏览器会话之间永久保存。
keywords: cookies;privacy
seo-description: Analytics 使用 Cookie 来提供有关变量和组件的信息，这类信息无法在图像请求和浏览器会话之间永久保存。
seo-title: 第一方 Cookie
solution: Experience Cloud,Analytics
title: 第一方 Cookie
index: y
snippet: y
translation-type: tm+mt
source-git-commit: b34cec87be58b9a4df3e9b061010689e5db4adb6
workflow-type: tm+mt
source-wordcount: '1460'
ht-degree: 99%

---


# 关于第一方 Cookie

Analytics 使用 Cookie 来提供有关变量和组件的信息，这类信息无法在图像请求和浏览器会话之间永久保存。这些源自 Adobe 托管域的无害 Cookie，称为第三方 Cookie。

许多浏览器和防间谍软件应用程序旨在拒绝并删除第三方 Cookie，包括 Analytics 数据收集中使用的 Cookie。为了支持您跟踪访客与网站的交互方式，您可以实施第一方 Cookie。

有两个方案可用来实施第一方 Cookie：

* Experience Platform ID 服务。这个 ID 服务可使用 JavaScript 在第一方上下文中设置 Cookie。
* 公司的 DNS 服务器上的 DNS 条目，用于为 Adobe 托管的域配置 CNAME 别名。请注意，尽管各种 Adobe 产品都支持使用 CNAME，但 CNAME 在任何情况下都用于为特定客户创建受信任的第一方端点，并且归此客户拥有。如果该客户控制多个域，则他们可能使用单个 CNAME 端点来跟踪其域内的用户，但由于这需要 CNAME 域外所有域的第三方 Cookie，因此当第三方 Cookie 被阻止时，它将不起作用，因而不建议使用。Adobe CNAME 从来不会用于跨不同客户拥有的域跟踪个人或设备。

即使将第一个方案与 Experience Cloud ID 服务结合使用，Apple 的 ITP 也会使第一方 Cookie 的生命周期缩短，因此最好将其与第二个方案结合使用。

对于使用 CNAME 的第二个方案，如果您的站点具有使用 HTTPS 协议的安全页面，则可以与 Adobe 合作获取 SSL 证书，以实施第一方 Cookie。Adobe 强烈建议您只使用 HTTPS 进行数据收集，因为我们将在 2020 年下半年停止对 HTTP 收集的支持。

SSL 证书的颁发过程往往令人感到混乱和费时。为此，Adobe 与行业领先的证书颁发机构 (CA) 建立了合作伙伴关系，并制定出一个集成式流程，进而实现了购买和管理这些证书的自动化。

在获得您的允许后，我们将与我们的 CA 一起为您颁发、部署和管理一个新的 SHA-2 SSL 证书。Adobe 将继续管理此证书，并确保意外的过期、撤销或安全问题不会威胁到贵组织安全集合的可用性。

## Adobe 管理的证书计划

为第一方 Cookie 实施新的第一方 SSL 证书时，建议使用 Adobe 管理的证书计划流程。

Adobe 管理的证书计划允许您为第一方 Cookie 实施新的第一方 SSL 证书，而不需增加任何额外费用（适用于您的前 100 个 CNAME）。如果您目前拥有自己的客户管理的 SSL 证书，请联系 Adobe 客户关怀部门，以便将其迁移到 Adobe 管理的证书计划。

### 实施

下面是如何为第一方 Cookie 实施新的第一方 SSL 证书的步骤：

1. 填写[第一方 Cookie 请求表](/help/interface/cookies/assets/FPC_Request_Form.xlsx)，并通过客户关怀部门开立一个票证，请求根据 Adobe 管理的证书计划设置第一方 Cookie。文档中通过示例描述了每个字段。

1. 创建 CNAME 记录（请参阅下面的说明）。

   当客户关怀代表收到票证后，将为您提供一对 CNAME 记录。您必须在贵公司的 DNS 服务器上配置这些记录，只有这样，Adobe 才能代表您购买证书。CNAMES 将与以下内容类似：

   **安全** - 例如，主机名 `smetrics.example.com` 指向：`example.com.ssl.d1.omtrdc.net`。

   **非安全** - 例如，主机名 `metrics.example.com` 指向：`example.com.d1.omtrdc.net`。

1. 配置了这些 CNAME 之后，Adobe 将与 DigiCert 一起购买证书并安装在 Adobe 的生产服务器上。

   如果您当前已经实施，则应当考虑使用“访客迁移”来维护现有访客。将证书实时推送到 Adobe 生产环境后，您就可以将跟踪服务器变量更新为新的主机名。也就是说，如果站点不安全 (HTTP)，则更新 `s.trackingServer` 变量。如果站点安全 (HTTPS)，则更新 `s.trackingServer` 和 `s.trackingServerSecure` 变量。

1. [验证主机名转发](#validate)（请参阅下文）。

1. [更新实施代码](#update)（请参阅下文）。

### 维护和续订

SSL 证书有效期为一年，这意味着 Adobe 必须每年为每个实施购买一个新证书。当每次实施接近失效期时，贵公司内的所有受支持用户都会收到一个电子邮件通知。为了让 Adobe 续订您的主机名，一位受支持的用户必须回复 Adobe 的电子邮件，并表明您计划继续使用即将到期的主机名进行数据收集。在这种情况下，Adobe 会自动购买并安装新证书。

### 常见问题解答

| 问题 | 回答 |
|---|---|
| **此过程是否安全？** | 是，Adobe 管理的证书计划较传统的方法更加安全，因为证书或私钥不会在 Adobe 和证书颁发机构的外部易手。 |
| **Adobe 如何为我们的域购买证书？** | 仅当您将指定的主机名（例如 `smetrics.example.com`）指向 Adobe 拥有的主机名时，Adobe 才能为您购买证书。这实质上是将此主机名委派给 Adobe，并允许 Adobe 代表您购买证书。 |
| **我是否可以请求吊销证书？** | 是，作为域所有者，您有权请求我们吊销证书。您只需通过客户关怀部门开立一个票证，即可完成此项操作。 |
| **此证书是否使用 SHA-2 加密？** | 是，Adobe 将与 DigicerT 一起颁发 SHA-2 证书。 |
| **这会产生任何额外费用吗？** | 不会，Adobe 可以向当前所有 Adobe Digital Experience 客户提供此服务，不会产生任何额外费用。 |

## 创建 CNAME 记录

贵组织的网络运营团队应通过创建新的 CNAME 记录来配置 DNS 服务器。每个主机名都将数据转发至 Adobe 的数据收集服务器。

FPC 专家为会您提供配置的主机名以及这些主机名所要指向的 CNAME。例如：

* **SSL 主机名**：`smetrics.mysite.com`
* **SSL CNAME**：`mysite.com.ssl.sc.omtrdc.net`
* **非 SSL 主机名**：`metrics.mysite.com`
* **非 SSL CNAME**：`mysite.com.sc.omtrdc.net`

只要没有更改实施代码，该步骤就不会影响数据收集，您可以在更新了实施代码后的任何时间，执行该步骤。

>[!NOTE]
>
>Experience Cloud 访客 ID 服务提供了配置 CNAME 以启用第一方 Cookie 的替代方法，但由于最近 Apple ITP 发生了更改，因此即便使用 Experience Cloud ID 服务，也建议分配 CNAME。

## 验证主机名转发 {#validate}

可以使用以下方法进行验证：

### 使用浏览器进行验证

如果已设置 CNAME 并且安装了证书，则可以使用浏览器进行验证：

`https://sstats.adobe.com/_check`

>[!NOTE]
>
>如果未安装证书，您将会看到安全警告。

### 使用 [!DNL curl] 进行验证

Adobe recommends using [[!DNL curl]](https://curl.haxx.se/) from the command line. （[!DNL Windows] 用户可以从以下位置安装 [!DNL curl]：<https://curl.haxx.se/windows/>）

如果您有 CNAME，但未安装证书，请运行：
`curl -k https://sstats.adobe.com/_check`
响应：`SUCCESS`

（`-k` 值将禁用安全警告。）

如果已设置 CNAME 并且安装了证书，请运行：
`curl https://sstats.adobe.com/_check`
响应：`SUCCESS`

### 使用 [!DNL nslookup] 进行验证

你可以使用 `nslookup` 进行验证。以 `sstats.adobe.com` 为例，打开命令提示符并键入 `nslookup sstats.adobe.com`

如果已成功设置一切，您将看到类似以下内容的返回：

```
nslookup sstats.adobe.com
Server:             10.30.7.247
Address:     10.30.7.247#53

sstats.adobe.com    canonical name = adobe.com.ssl.d1.sc.omtrdc.net.
Name:  adobe.com.ssl.d1.sc.omtrdc.net
Address: 54.218.180.161
Name:  adobe.com.ssl.d1.sc.omtrdc.net
Address: 52.39.8.230
Name:  adobe.com.ssl.d1.sc.omtrdc.net
Address: 54.187.216.46
```

## 更新实施代码 {#update}

在网站上编辑代码以使用第一方 Cookie 之前，请完成以下前提条件：

* 按照上文 [Adobe 管理的证书计划](#adobe-managed-certificate-program)的&#x200B;*实施*&#x200B;部分中描述的步骤，请求 SSL 证书。
* 创建 CNAME 记录（请参阅上文）。
* 验证主机名（请参阅上文）。

在您验证主机名能够响应并转发到 Adobe 数据收集服务器后，您可以更改实施以指向您自己的数据收集主机名。

1. 打开您的核心 Javascript 文件 (`s_code.js/AppMeasurement.js`)。
1. 如果您想要更新您的代码版本，请使用较新版本替换整个 `s_code.js/AppMeasurement.js` 文件，然后替换任意插件或自定义设置（如果有）。**或者**，如果您只想更新与第一方 Cookie 相关的代码，请找到 s.trackingServer 和 s.trackingServerSecure（如果使用 SSL）变量，并将它们指向您的新数据收集主机名。以 mysite.com 为例：`s.trackingServer = "metrics.mysite.com"``s.trackingServerSecure = "smetrics.mysite.com"`

1. 将更新后的核心 Javascript 文件上传到您的网站。

1. 如果您从一个长期存在的实施移至第一方 Cookie，或更改为其他第一方收集主机名，我们建议您将访客从先前的域迁移至新域。

请参阅“Analytics 实施指南”中的[访客迁移](https://docs.adobe.com/help/en/analytics/implementation/javascript-implementation/visitor-migration.html)。

在上传了该 JavaScript 文件后，将针对第一方 Cookie 数据收集完成所有相应的配置。我们建议您在接下来的几个小时监控 Analytics 报告，以确保数据收集持续正常进行。如果未能正常进行数据收集，请验证上述所有步骤是否已经完成，并安排贵组织的一名受支持用户联系客户关怀部门。
