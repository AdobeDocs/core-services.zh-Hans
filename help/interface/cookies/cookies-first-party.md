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
source-git-commit: 64d35205275317e46072e7239b52863bf3b34e12

---


# 关于第一方 Cookie

Analytics 使用 Cookie 来提供有关变量和组件的信息，这类信息无法在图像请求和浏览器会话之间永久保存。这些无害的cookies源自Adobe托管的域，称为第三方cookies。

许多浏览器和防间谍软件应用程序旨在拒绝并删除第三方 Cookie，包括 Analytics 数据收集中使用的 Cookie。为了支持跟踪访客与网站的交互方式，您可以实施第一方Cookie。

可使用两个选项来实施第一方Cookie:

* Experience Platform ID 服务。这个 ID 服务可使用 JavaScript 在第一方上下文中设置 Cookie。
* 公司DNS服务器上的DNS条目，用于将CNAME别名配置为Adobe托管域。 请注意，虽然各种Adobe产品支持使用CNAME，但在所有情况下，CNAME都用于为特定客户创建可信的第一方端点，且该客户拥有该端点。 如果客户控制多个域，则他们可能使用单个CNAME端点跨域跟踪用户，但这要求CNAME域外的所有域都有第三方Cookie，因此当第三方Cookie被阻止时，它不起作用，因此不建议这样做。 Adobe CNAME永远不会用于跨不同客户拥有的域跟踪个人或设备。

即使将第一个选项与Experience Cloud ID服务结合使用，Apple的ITP也会使第一方Cookie短期有效，因此最好将其与第二个选项结合使用。

对于使用CNAME的第二个选项，如果您的站点具有使用HTTPS协议的安全页面，则可以与Adobe一起获取SSL证书以实施第一方Cookie。 Adobe强烈建议您只使用HTTPS进行数据收集，因为我们将在2020年下半年放弃对HTTP收集的支持。

SSL 证书的颁发过程往往令人感到混乱和费时。为此，Adobe 与行业领先的证书颁发机构 (CA) 建立了合作伙伴关系，并制定出一个集成式流程，进而实现了购买和管理这些证书的自动化。

在获得您的允许后，我们将与我们的 CA 一起为您颁发、部署和管理一个新的 SHA-2 SSL 证书。Adobe将继续管理此证书，并确保意外的过期、撤销或安全问题不会威胁组织的安全集合的可用性。

## Adobe 管理的证书计划

为第一方 Cookie 实施新的第一方 SSL 证书时，建议使用 Adobe 管理的证书计划流程。

Adobe 管理的证书计划允许您在不增加任何额外费用的情况下，为第一方 Cookie 实施新的第一方 SSL 证书。如果您目前拥有自己的客户管理的 SSL 证书，请联系 Adobe 客户关怀部门，以便将其迁移到 Adobe 管理的证书计划。

### 实施

下面是如何为第一方 Cookie 实施新的第一方 SSL 证书的步骤：

1. 填写[第一方 Cookie 请求表](/help/interface/cookies/assets/FPC_Request_Form.xlsx)，并通过客户关怀部门开立一个票证，请求根据 Adobe 管理的证书计划设置第一方 Cookie。文档中通过示例描述了每个字段。

1. 创建 CNAME 记录（请参阅下面的说明）。

   收到票证后，客户关怀代表应为您提供一对CNAME记录。 您必须在贵公司的 DNS 服务器上配置这些记录，只有这样，Adobe 才能代表您购买证书。CNAMES将类似于：

   **安全** -例如，主机名指 `smetrics.example.com` 向： `example.com.ssl.d1.omtrdc.net`.

   **非安全** - 例如，主机名 `metrics.example.com` 指向：`example.com.d1.omtrdc.net`。

1. 配置了这些 CNAME 之后，Adobe 将与 DigiCert 一起购买证书并安装在 Adobe 的生产服务器上。

   如果您有现有实施，则应考虑迁移访客以维护现有访客。 在将证书实时推送到Adobe的生产环境后，您可以将跟踪服务器变量更新为新的主机名。 Meaning, if the site is not secure (HTTP), update the `s.trackingServer`. If the site is secure (HTTPS), update both `s.trackingServer` and `s.trackingServerSecure` variables.

1. [验证主机名转发](#validate) （请参阅下文）。

1. [更新实施代码](#update) （请参阅下文）。

### 维护和续订

SSL 证书有效期为一年，这意味着 Adobe 必须每年为每个实施购买一个新证书。当每次实施接近失效期时，贵公司内的所有受支持用户都会收到一个电子邮件通知。要使Adobe续订您的主机名，一个受支持的用户必须回复Adobe发送的电子邮件，并指示您计划继续使用即将过期的主机名进行数据收集。 在这种情况下，Adobe 会自动购买并安装新证书。

### 常见问题解答

| 问题 | 回答 |
|---|---|
| **此过程是否安全？** | 是，Adobe 管理的证书计划较传统的方法更加安全，因为证书或私钥不会在 Adobe 和证书颁发机构的外部易手。 |
| **Adobe 如何为我们的域购买证书？** | 仅当您将指定的主机名（例如 smetrics.example.com）指向 Adobe 拥有的主机名时，Adobe 才能为您购买证书。这实质上是将此主机名委派给 Adobe，并允许 Adobe 代表您购买证书。 |
| **我是否可以请求吊销证书？** | 是，作为域所有者，您有权请求我们吊销证书。您只需通过客户关怀部门开立一个票证，即可完成此项操作。 |
| **此证书是否使用 SHA-2 加密？** | 是，Adobe 将与 DigicerT 一起颁发 SHA-2 证书。 |
| **这会产生任何额外费用吗？** | 否，Adobe将免费向所有当前的Adobe数字体验客户提供此服务。 |

## 创建 CNAME 记录

贵组织的网络运营团队应通过创建新的 CNAME 记录来配置 DNS 服务器。每个主机名都将数据转发至 Adobe 的数据收集服务器。

FPC 专家为会您提供配置的主机名以及这些主机名所要指向的 CNAME。例如：

* **SSL 主机名**：`smetrics.mysite.com`
* **SSL CNAME**：`mysite.com.ssl.sc.omtrdc.net`
* **非 SSL 主机名**：`metrics.mysite.com`
* **非 SSL CNAME**：`mysite.com.sc.omtrdc.net`

只要没有更改实施代码，该步骤就不会影响数据收集，您可以在更新了实施代码后的任何时间，执行该步骤。

>[!N注意：]
>Experience Cloud访客ID服务为配置CNAME以启用第一方Cookie提供了一种替代方法，但由于Apple ITP最近发生了更改，因此，即使在使用Experience Cloud ID服务时，仍建议您分配CNAME。

## 验证主机名转发 {#validate}

可以使用以下方法进行验证：

### 使用浏览器验证

如果设置了CNAME并安装了证书，则可以使用浏览器进行验证：

`https://sstats.adobe.com/_check`

**注意：** 如果未安装证书，您将看到安全警告。

### 验证方式 [!DNL curl]

Adobe建议从命令行 [使用](https://curl.haxx.se/)[!DNL curl]。 (用[!DNL Windows] 户可以从以下 [!DNL curl] 位置安装： <https://curl.haxx.se/windows/>)

如果您有CNAME但未安装证书，请运行：响`curl -k https://sstats.adobe.com/_check`应： `SUCCESS`

(该值 `-k` 将禁用安全警告。)

如果设置了CNAME并安装了证书，请运行：响`curl https://sstats.adobe.com/_check`应： `SUCCESS`

### 验证方式 [!DNL nslookup]

可用于 `nslookup` 验证。 以 `sstats.adobe.com`示例为例，打开命令提示并键入 `nslookup sstats.adobe.com`

如果一切都成功设置，您将看到类似以下内容的返回：

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

* 按照 *Adobe Managed Certificate Program的“实施* ”部分中所述的步骤请求 [SSL证书](#adobe-managed-certificate-program)。
* 创建 CNAME 记录（请参阅上文）。
* 验证主机名（请参阅上文）。

在您验证主机名能够响应并转发到 Adobe 数据收集服务器后，您可以更改实施以指向您自己的数据收集主机名。

1. 打开您的核心 Javascript 文件 (`s_code.js/AppMeasurement.js`)。
1. 如果您想要更新您的代码版本，请使用较新版本替换整个 `s_code.js/AppMeasurement.js` 文件，然后替换任意插件或自定义设置（如果有）。**或者**，如果您只想更新与第一方 Cookie 相关的代码，请找到 s.trackingServer 和 s.trackingServerSecure（如果使用 SSL）变量，并将它们指向您的新数据收集主机名。以 mysite.com 为例：`s.trackingServer = "metrics.mysite.com"``s.trackingServerSecure = "smetrics.mysite.com"`

1. 将更新后的核心 Javascript 文件上传到您的网站。

1. 如果您从一个长期存在的实施移至第一方 Cookie，或更改为其他第一方收集主机名，我们建议您将访客从先前的域迁移至新域。

请参 [阅《分析实施指南](https://docs.adobe.com/help/en/analytics/implementation/javascript-implementation/visitor-migration.html) 》中的访客迁移。

在上传了该 JavaScript 文件后，将针对第一方 Cookie 数据收集完成所有相应的配置。我们建议您在接下来的几个小时监控 Analytics 报告，以确保数据收集持续正常进行。如果未能正常进行数据收集，请验证上述所有步骤是否已经完成，并安排贵组织的一名受支持用户联系客户关怀部门。
