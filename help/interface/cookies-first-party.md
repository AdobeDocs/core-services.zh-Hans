---
description: 了解 Adobe Analytics 如何使用 Cookie 来提供有关变量和组件的信息，这类信息无法在图像请求和浏览器会话之间永久保存。
solution: Experience Cloud,Analytics
title: "第一方 Cookie "
index: y
snippet: y
feature: Cookies
topic: Administration
role: Admin
level: Experienced
exl-id: e15abde5-8027-4aed-a0c1-8a6fc248db5e
source-git-commit: f5cead10ecfeefeb560e92881524650e55bd938d
workflow-type: tm+mt
source-wordcount: '1636'
ht-degree: 78%

---

# 关于第一方 Cookie

Analytics 使用 Cookie 来提供有关变量和组件的信息，这类信息无法在图像请求和浏览器会话之间永久保存。Adobe 尽可能使用第一方 Cookie 记录您网站上的活动。记录不同网站（如您可能拥有的其他域）上的活动需要使用第三方 cookie。

许多浏览器和防间谍软件应用程序都设计为拒绝并删除第三方 Cookie。Adobe 确保我们始终可以设置 Cookie，即使第三方 Cookie 被阻止也是如此。具体行为会因您使用的是Experience Platform标识服务（ECID服务）还是Analytics的旧版标识符（即s_vi Cookie）而异：

* [Experience Platform Identity Service（ECID 服务）](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html?lang=en)将自动设置第一方 Cookie，无论您的收集域是否与网站域匹配。如果二者不匹配，Identity服务将使用JavaScript在您网站的域中设置Cookie。
* 如果使用 [Analytics 旧版标识符](https://experienceleague.adobe.com/docs/core-services/interface/administration/ec-cookies/cookies-analytics.html?lang=en)（又称 `s_vi` Cookie），则它将取决于您配置数据收集服务器的方式。如果数据收集服务器与您网站的域相同，则 Cookie 被设置为第一方。如果收集服务器与您当前的域不同，则 Cookie 被设置为第三方。在这种情况下，如果第三方 Cookie 被阻止，则 Analytics 将设置第一方[后备 ID (s_fid)](cookies-analytics.md) 而非标准“s_vi”Cookie。

如果您希望确保收集服务器与网站的域相匹配，则可以使用CNAME实施，该实施将允许从CNAME实施中指定的自定义域转发到Adobe的收集服务器。 其中涉及更改您公司的 DNS 设置以配置指向某个 Adobe 托管域的 CNAME 别名。请注意，尽管多种 Adobe 产品都支持使用 CNAME，但在所有情况下 CNAME 都用于为特定客户创建受信任的第一方端点，并归该客户拥有。如果您控制多个域，则它们可使用单个 CNAME 端点在其域间跟踪用户，但是，只要网站域与 CNAME 域不同，Cookie 就被设置为第三方。

>[!NOTE]
>
>无论您的收集域是否与您的网站域相匹配，Apple的智能防跟踪(ITP)程序都会使由Adobe设置的第一方Cookie在受ITP管辖的浏览器(包括macOS上的Safari以及iOS和iPadOS上的所有浏览器)上短暂存留。 自 2020 年 11 月起，通过 CNAME 设置的 Cookie 与通过 JavaScript 设置的 Cookie 具有相同的有效期。此有效期可能会有变化。

如果您要为数据收集建立 CNAME，并且您的网站具有使用 HTTPS 协议的安全页面，则可以与 Adobe 合作以获取 SSL 证书。

SSL 证书的颁发过程往往令人感到混乱和费时。为此，Adobe 与 DigiCert 这一行业领先的证书颁发机构 (CA) 建立了合作伙伴关系，并制定出一个集成式流程，进而实现了购买和管理这些证书的自动化。

在获得您的允许后，我们与 CA 一起为您颁发、部署和管理一个新的 SHA-2 SSL 证书。Adobe 会继续管理此证书，并确保意外的过期、撤销或安全问题不会威胁到贵组织安全集合的可用性。

## Adobe 管理的证书计划

Adobe 管理的证书计划是用于设置 CNAME 实施所需的第一方 SSL 证书的推荐流程，可确保您的 Adobe 收集服务器与网站域相匹配。

利用 Adobe 管理的证书计划，您可以实施新的第一方 SSL 证书，而不会产生额外费用（适用于前 100 个 CNAME）。如果您目前拥有自己的客户管理的 SSL 证书，请联系 Adobe 客户关怀部门，以便将其迁移到 Adobe 管理的证书计划。

### 实施

下面说明了如何为第一方数据收集实施新的第一方 SSL 证书：

1. 填写[第一方域请求表](/help/interface/cookies/assets/First_Part_Domain_Request_Form.xlsx)，并通过客户关怀部门开立一个票证，请求根据 Adobe 管理的计划设置第一方数据收集。

   文档中通过示例描述了每个字段。

1. 创建 CNAME 记录（请参阅下面的说明）。

   在收到服务单后，客户关怀代表应为您提供 CNAME 记录。必须在贵公司的 DNS 服务器上配置这些记录，然后 Adobe 才能代表您购买证书。该 CNAME 类似于以下内容：

   **安全** - 例如，主机名 `smetrics.example.com` 指向：`example.com.adobedc.net`。

   >[!NOTE]
   > 过去，Adobe建议客户设置两个CNAME，一个用于HTTPS，一个用于HTTP。 由于加密流量是最佳做法，而且大多数浏览器都强烈阻止使用HTTP，因此我们不再建议为HTTP设置CNAME。 现在，将这两者都设置为最佳实践 `trackingServer` 和 `trackingServerSecure` 的CNAME。 例如， `trackingServer` 和 `trackingServerSecure` 将设置为 `smetrics.example.com`. HTTP仅允许用于第三方主机名。

1. 设置好 CNAME 后，Adobe 与 DigiCert 合作以购买证书并安装到 Adobe 的生产服务器上。

   如果您当前已经实施，则应当考虑使用“访客迁移”来维护现有访客。将证书实时推送到Adobe的生产环境后，您可以将跟踪服务器变量更新为新的主机名。 也就是说，如果站点不安全 (HTTP)，则更新 `s.trackingServer` 变量。如果站点安全 (HTTPS)，则更新 `s.trackingServer` 和 `s.trackingServerSecure` 变量。

1. [验证主机名转发](#validate)（请参阅下文）。

1. [更新实施代码](#update)（请参阅下文）。

### 维护和续订

在第一方证书过期的三十天前，Adobe会验证CNAME是否仍然有效且正在使用。 如果是，则Adobe假定您要继续使用服务并代表您自动重新发布证书。

此时，如果CNAME已删除且不再有效，则Adobe不会续订证书，并且系统中的条目将标记为删除。 如果已删除CNAME，则Adobe知道尚未使用该URL进行跟踪，因此可以安全地删除该URL。

### 常见问题解答

| 问题 | 回答 |
|---|---|
| **此过程是否安全？** | 是，Adobe 管理的证书计划较传统的方法更加安全，因为证书或私钥不会在 Adobe 和证书颁发机构的外部易手。 |
| **Adobe 如何为我们的域购买证书？** | 仅当您将指定的主机名（例如 `telemetry.example.com`）指向 Adobe 拥有的主机名时，Adobe 才能为您购买证书。这实质上是将此主机名委派给 Adobe，并允许 Adobe 代表您购买证书。 |
| **我是否可以请求吊销证书？** | 是，作为域的所有者，您有权请求吊销证书。 通过客户关怀部门开具票证，以完成此操作。 |
| **此证书是否使用 SHA-2 加密？** | 是，Adobe可与DigiCert一起颁发SHA-2证书。 |
| **这会产生任何额外费用吗？** | 不会，Adobe 可以向当前所有 Adobe Digital Experience 客户提供此服务，不会产生任何额外费用。 |

{style=&quot;table-layout:auto&quot;}

## 创建 CNAME 记录

贵组织的网络运营团队应通过创建 CNAME 记录来配置 DNS 服务器。每个主机名都将数据转发至 Adobe 的数据收集服务器。

FPC 专家为您提供所配置的主机名及其要指向哪个 CNAME。例如：

* **SSL 主机名**：`smetrics.mysite.com`
* **SSL CNAME**：`mysite.com.adobedc.net`

>[!NOTE]
> 如果您仍使用非安全方式，则它看上去将类似于此。
> * **非 SSL 主机名**：`metrics.mysite.com`
> * **非 SSL CNAME**：`mysite.com.adobedc.net`


只要没有更改实施代码，该步骤就不会影响数据收集，您可以在更新了实施代码后的任何时间，执行该步骤。

## 验证主机名转发 {#validate}

可以使用以下方法进行验证：

### 使用浏览器进行验证

如果已设置 CNAME 并且安装了证书，则可以使用浏览器进行验证：

`https://smetrics.adobe.com/_check`

>[!NOTE]
>
>如果未安装证书，您会看到安全警告。

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

如果已成功设置一切，您会看到类似以下内容的返回：

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

在网站上编辑代码以使用第一方数据收集之前，请完成以下前提条件：

* 按照 [Adobe 管理的证书计划](#adobe-managed-certificate-program)的&#x200B;*实施*&#x200B;部分中描述的步骤，请求 SSL 证书。
* 创建 CNAME 记录（请参阅上文）。
* 验证主机名（请参阅上文）

在您验证主机名能够响应并转发到 Adobe 数据收集服务器后，您可以更改实施以指向您自己的数据收集主机名。

1. 打开您的核心 Javascript 文件 (`s_code.js/AppMeasurement.js`)。
1. 如果您想要更新您的代码版本，请使用较新版本替换整个 `s_code.js/AppMeasurement.js` 文件，然后替换任意插件或自定义设置（如果有）。**或者**，如果您只想更新与第一方数据收集相关的代码，请找到 s.trackingServer 和 s.trackingServerSecure（如果使用 SSL）变量，并将它们指向您的新数据收集主机名。以 mysite.com 为例：`s.trackingServer = "metrics.mysite.com"``s.trackingServerSecure = "smetrics.mysite.com"`

1. 将更新后的核心 Javascript 文件上传到您的网站。

1. 如果您从一个长期存在的实施移至第一方数据收集，或更改为其他第一方收集主机名，Adobe 建议您将访客从先前的域迁移至新域。

请参阅“Analytics 实施指南”中的[访客迁移](https://experienceleague.adobe.com/docs/analytics/technotes/visitor-migration.html?lang=en)。

在上传了 JavaScript 文件后，将针对第一方数据收集完成所有相应的配置。Adobe 建议您在接下来的几个小时监控 Analytics 报告，以确保数据收集持续正常进行。如果未能正常进行数据收集，请验证上述所有步骤是否已经完成，并安排贵组织的一名受支持用户联系客户关怀部门。
