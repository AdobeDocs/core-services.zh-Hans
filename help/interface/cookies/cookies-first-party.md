---
description: 了解 Adobe Analytics 如何使用 Cookie 来提供有关变量和组件的信息，这类信息无法在图像请求和浏览器会话之间永久保存。
keywords: cookies;隐私
solution: Experience Cloud,Analytics
title: '"第一方 Cookie "'
index: y
snippet: y
feature: Cookie
topic: 管理
role: Administrator
level: Experienced
exl-id: e15abde5-8027-4aed-a0c1-8a6fc248db5e
source-git-commit: f720e37b693da2c657cb1efab45620c60bfa81a4
workflow-type: tm+mt
source-wordcount: '1594'
ht-degree: 60%

---

# 关于第一方 Cookie

Analytics 使用 Cookie 来提供有关变量和组件的信息，这类信息无法在图像请求和浏览器会话之间永久保存。Adobe 尽可能使用第一方 Cookie 记录您网站上的活动。记录不同网站（如您可能拥有的其他域）上的活动需要使用第三方 cookie。

许多浏览器和反间谍软件应用程序旨在拒绝和删除第三方Cookie，包括[!DNL Analytics]数据收集中使用的Cookie。 要支持跟踪访问者如何与您的网站进行交互，您应确保已将数据收集配置为使用第一方 Cookie：

有两种方式可用于实现第一方 Cookie：

* 如果您使用的是Experience Platform标识服务（ECID服务），它会使用JavaScript在第一方上下文中自动设置Cookie。
* 如果您使用的是[!DNL Analytics]旧版标识符（即`s_vi` Cookie），则取决于您如何配置数据收集服务器。 如果数据收集服务器与您网站的域相匹配，则Cookie将设置为第一方。 如果收集服务器与您的当前域不匹配，则Cookie将设置为第三方。 在这种情况下，如果阻止第三方Cookie，[!DNL Analytics]将设置第一方[回退id(&quot;s_fid&quot;)](https://experienceleague.adobe.com/docs/core-services/interface/ec-cookies/cookies-analytics.html?lang=zh-Hans#section-65e33f9bfc264959ac1513e2f4b10ac7)，而不是标准的“s_vi”Cookie。

为确保您的收集服务器与您网站的域相匹配，您可以使用允许在第一方上下文中设置Cookie的CNAME实施。 其中涉及更改您公司的 DNS 设置以配置指向某个 Adobe 托管域的 CNAME 别名。请注意，尽管多种 Adobe 产品都支持使用 CNAME，但在所有情况下 CNAME 都用于为特定客户创建受信任的第一方端点，并归该客户拥有。如果您控制多个域，则他们可能使用单个CNAME端点来跟踪其域中的用户，但只要网站域与CNAME域Cookie不匹配，则会将其设置为第三方。

>[!NOTE]
>
>对于这两个选项，Apple的智能防跟踪(ITP)程序都会使第一方Cookie在受ITP管理的浏览器（包括macOS上的Safari以及iOS和iPadOS上的所有浏览器）上短暂存在。 从 2020 年 11 月起，这两种类型的 Cookie 均为 7 天内有效。此有效期可能会有变化。

对于使用 CNAME 的第二个方案，如果您的站点具有使用 HTTPS 协议的安全页面，则可以与 Adobe 合作获取 SSL 证书，以实施第一方 Cookie。Adobe强烈建议您专门使用HTTPS进行数据收集，因为Adobe在2020年下半年不再支持HTTP收集。

SSL 证书的颁发过程往往令人感到混乱和费时。因此，Adobe与行业领先的证书颁发机构(CA)建立了合作伙伴关系，并开发了一个集成式流程，通过该流程可自动购买和管理这些证书。

在获得您的许可后，我们与CA合作，为您颁发、部署和管理新的SHA-2 SSL证书。 Adobe将继续管理此证书，并确保意外的过期、撤销或安全问题不会威胁到贵组织安全集合的可用性。

## Adobe管理的证书计划

为第一方 Cookie 实施新的第一方 SSL 证书时，建议使用 Adobe 管理的证书计划流程。

Adobe 管理的证书计划允许您为第一方 Cookie 实施新的第一方 SSL 证书，而不需增加任何额外费用（适用于您的前 100 个 CNAME）。如果您当前拥有自己的客户管理SSL证书，请与Adobe客户关怀团队联系，以了解如何迁移到Adobe管理的证书计划。

### 实施

下面是如何为第一方 Cookie 实施新的第一方 SSL 证书的步骤：

1. 填写[第一方Cookie请求表](/help/interface/cookies/assets/First_Part_Domain_Request_Form.xlsx)，并与客户关怀部门开立一个票证，请求在Adobe管理的程序上设置第一方Cookie。 文档中通过示例描述了每个字段。

2. 创建 CNAME 记录（请参阅下面的说明）。

   在收到服务单后，客户关怀代表应为您提供 CNAME 记录。必须在贵公司的 DNS 服务器上配置这些记录，然后 Adobe 才能代表您购买证书。CNAME类似于以下内容：

   **安全** - 例如，主机名 `smetrics.example.com` 指向：`example.com.adobedc.net`。

>[!NOTE]
> 过去，Adobe建议客户设置两个CNAME，一个用于HTTPS，一个用于HTTP。 由于将流量加密是一项最佳实践，并且大多数浏览器都极力阻止使用 HTTP，因此我们不再建议为 HTTP 设置 CNAME。如果需要，将如下所示：
>    **不安全** - 主机名 `metrics.example.com` 指向：`example.com.adobedc.net`。

1. CNAME到位后，Adobe将与DigiCert合作，购买证书并在Adobe的生产服务器上安装该证书。

   如果您当前已经实施，则应当考虑使用“访客迁移”来维护现有访客。将证书实时推送到 Adobe 生产环境后，您就可以将跟踪服务器变量更新为新的主机名。也就是说，如果站点不安全 (HTTP)，则更新 `s.trackingServer` 变量。如果站点安全 (HTTPS)，则更新 `s.trackingServer` 和 `s.trackingServerSecure` 变量。

2. [验证主机名转发](#validate)（请参阅下文）。

3. [更新实施代码](#update)（请参阅下文）。

### 维护和续订

SSL 证书有效期为一年，这意味着 Adobe 必须每年为每个实施购买一个新证书。每当实施接近到期时，您组织内的所有受支持用户都会收到一封电子邮件通知。 为了让 Adobe 续订您的主机名，一位受支持的用户必须回复 Adobe 的电子邮件，并表明您计划继续使用即将到期的主机名进行数据收集。在这种情况下，Adobe 会自动购买并安装新证书。

### 常见问题

| 问题 | 回答 |
|---|---|
| **此过程是否安全？** | 是的，由Adobe管理的程序比我们的旧版方法更加安全，因为证书或私钥不会在Adobe和颁发证书颁发机构之外易手。 |
| **Adobe 如何为我们的域购买证书？** | 仅当您将指定的主机名（例如 `telemetry.example.com`）指向 Adobe 拥有的主机名时，Adobe 才能为您购买证书。这实质上是将此主机名委派给 Adobe，并允许 Adobe 代表您购买证书。 |
| **我是否可以请求吊销证书？** | 是，作为域所有者，您有权请求我们吊销证书。您只需通过客户关怀部门开立一个票证，即可完成此项操作。 |
| **此证书是否使用 SHA-2 加密？** | 是，Adobe 将与 DigicerT 一起颁发 SHA-2 证书。 |
| **这会产生任何额外费用吗？** | 不会，Adobe 可以向当前所有 Adobe Digital Experience 客户提供此服务，不会产生任何额外费用。 |

## 创建 CNAME 记录

贵组织的网络运营团队应通过创建CNAME记录来配置DNS服务器。 每个主机名都将数据转发至 Adobe 的数据收集服务器。

FPC 专家为您提供所配置的主机名及其要指向哪个 CNAME。例如：

* **SSL 主机名**：`smetrics.mysite.com`
* **SSL CNAME**：`mysite.com.adobedc.net`

>[!NOTE]
> 如果您仍使用非安全，则将如下所示：
> * **非 SSL 主机名**：`metrics.mysite.com`
> * **非 SSL CNAME**：`mysite.com.adobedc.net`


只要没有更改实施代码，该步骤就不会影响数据收集，您可以在更新了实施代码后的任何时间，执行该步骤。

>[!NOTE]
>
>Experience Cloud 访客 ID 服务提供一种配置 CNAME 以启用第一方 Cookie 的替代方法。

## 验证主机名转发 {#validate}

可以使用以下方法进行验证：

### 使用浏览器进行验证

如果已设置 CNAME 并且安装了证书，则可以使用浏览器进行验证：

`https://smetrics.adobe.com/_check`

>[!NOTE]
>
>如果未安装证书，系统会向您发出安全警告。

### 使用 [!DNL curl] 进行验证

Adobe 建议从命令行中使用 [[!DNL curl]](https://curl.se/)。（[!DNL Windows] 用户可以从以下位置安装 [!DNL curl]：<https://curl.se/windows/>）

如果您有 CNAME，但未安装证书，请运行：
`curl -k https://smetrics.adobe.com/_check`
响应：`SUCCESS`

（`-k` 值将禁用安全警告。）

如果已设置 CNAME 并且安装了证书，请运行：
`curl https://smetrics.adobe.com/_check`
响应：`SUCCESS`

### 使用 [!DNL nslookup] 进行验证

你可以使用 `nslookup` 进行验证。以 `smetrics.adobe.com` 为例，打开命令提示符并键入 `nslookup smetrics.adobe.com`

如果一切设置成功，您将看到类似以下内容的返回：

```
nslookup smetrics.adobe.com
Server:             10.30.7.247
Address:     10.30.7.247#53

smetrics.adobe.com    canonical name = adobe.com.ssl.d1.sc.omtrdc.net.
Name:  adobe.com.ssl.d1.sc.omtrdc.net
Address: 54.218.180.161
Name:  adobe.com.ssl.d1.sc.omtrdc.net
Address: 52.39.8.230
Name:  adobe.com.ssl.d1.sc.omtrdc.net
Address: 54.187.216.46
```

## 更新实施代码 {#update}

在您的网站上编辑代码以使用第一方Cookie之前，请完成以下先决条件：

* 请求SSL证书，方法是按照上面[Adobe管理的证书程序](#adobe-managed-certificate-program)的&#x200B;*实施*&#x200B;部分中描述的步骤进行。
* 创建 CNAME 记录（请参阅上文）。
* 验证主机名（请参阅上文）。

在您验证主机名对Adobe数据收集服务器做出响应和转发后，您可以更改实施以指向您自己的数据收集主机名。

1. 打开您的核心 Javascript 文件 (`s_code.js/AppMeasurement.js`)。
1. 如果您想要更新您的代码版本，请使用较新版本替换整个 `s_code.js/AppMeasurement.js` 文件，然后替换任意插件或自定义设置（如果有）。**或者**，如果您只想更新与第一方 Cookie 相关的代码，请找到 s.trackingServer 和 s.trackingServerSecure（如果使用 SSL）变量，并将它们指向您的新数据收集主机名。以 mysite.com 为例：`s.trackingServer = "metrics.mysite.com"``s.trackingServerSecure = "smetrics.mysite.com"`

1. 将更新后的核心 Javascript 文件上传到您的网站。

1. 如果您从长期存在的实施转移到第一方Cookie，或更改为其他第一方收集主机名，则Adobe建议将访客从先前的域迁移到新域。

请参阅“Analytics 实施指南”中的[访客迁移](https://experienceleague.adobe.com/docs/analytics/implementation/javascript-implementation/visitor-migration.html?lang=en)。

在上传了该 JavaScript 文件后，将针对第一方 Cookie 数据收集完成所有相应的配置。Adobe建议您在接下来的几小时内监控Analytics报表，以确保数据收集继续正常进行。 如果未能正常进行数据收集，请验证上述所有步骤是否已经完成，并安排贵组织的一名受支持用户联系客户关怀部门。
