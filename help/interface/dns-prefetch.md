---
description: 对不同的解决方案和服务实施 DNS 预获取，以帮助缩短页面加载时间。
seo-description: 对不同的解决方案和服务实施 DNS 预获取，以帮助缩短页面加载时间。
seo-title: 使用不同解决方案和服务的DNS预购
solution: Experience Cloud
title: 使用不同解决方案和服务的DNS预购
uuid: 4220e223e00e-46b1-8bde-52248913ba1
translation-type: tm+mt
source-git-commit: af5339fe58ce884345804574c209907d6504a483

---


# 使用不同解决方案和服务的DNS预购

对不同的解决方案和服务实施 DNS 预获取，以帮助缩短页面加载时间。

## 了解DNS抢占 {#section_772BF9CB7C4141DE9B0355146E2CD962}

浏览器使用 DNS 预获取自动将 Web 页面上链接的域名解析为相应的 IP 地址。当您的浏览器加载 Web 页面时，预获取过程便会开始。例如，例如，您的页面包含可单击的链接 `www.adobe.com`。当浏览器加载此页面时，便会使用 [DNS 系统](https://www.networksolutions.com/support/what-is-a-domain-name-server-dns-and-how-does-it-work/)查找链接的域名，并将其解析为相应的数字 IP 地址。DNS 预获取可帮助提升页面性能，因为在站点访客单击该链接或按钮之前，域名已经解析为 IP 地址。DNS 预获取过程对用户是透明的。

## DNS印前检查和Adobe Experience Cloud解决方案 {#section_202A07F9F79F4ABDA44B98BA1DDCD516}

DNS 预获取会自动处理页面上嵌入的静态链接。这也意味着自动 DNS 预获取不能用于不同的 [!UICONTROL Experience Cloud] 解决方案和服务，因为：

* 当页面加载时，每个 Experience Cloud 解决方案或服务都会动态生成 DNS 调用。
* 只有在执行这些调用之后，浏览器才能将域名解析为 IP 地址。

但是，您可以手动在 Experience Cloud 解决方案中实施 DNS 预获取。为此，您可以将HTML `<dns-prefetch>` 标记添加到页面代码的 `<head>` 部分，如下所示。正确实施后，DNS 预获取可使页面加载时间缩短数毫秒。

## DNS预捕获代码范例 {#section_E886F7B2861E48BA9EF3D8B3CE32B345}

下面的示例说明了如何对不同的 [!DNL Experience Cloud] 解决方案和服务执行 DNS 预获取调用。有些预获取调用需要使用您的 [!DNL Adobe] 组织 ID 或跟踪服务器信息。在这些示例中，*斜体*格式的代码表示变量占位符。您需要将这些代码替换为您自己的 [!DNL Adobe] 合作伙伴 ID、客户代码或跟踪服务器信息等。

* **Analytics:** `<link rel="dns-prefetch" href="//insert tracking server name here">`.

   如果您使用非安全或安全跟踪服务器，请为每个 DNS 名称添加单独的标记。

* **Audience Manager:** `<link rel="dns-prefetch" href="//dpm.demdex.net">`

* **Experience Cloud ID服务：**`<link rel="dns-prefetch" href="//fast. *`在此处插入合作伙伴ID`*.demdex.net">`

* **Dynamic Tag Manager** (DTM)：不需要。当页面开始加载时，即可使用 DTM 链接。

* **Media Optimizer(Ad Cloud)：**

   * `<link rel="dns-prefetch" href="//pixel.everesttech.net">`
   * `<link rel="dns-prefetch" href="//cm.everesttechnet">`


* **Target:** `<link rel="dns-prefetch" href="//insert customer code here.tt.omtrdc.net">`

>[!MORE_ LIKE_ This]
>
>* [DNS 预获取](https://www.chromium.org/developers/design-documents/dns-prefetching)

