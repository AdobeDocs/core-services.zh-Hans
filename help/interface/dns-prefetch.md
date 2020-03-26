---
description: 对不同的解决方案和服务实施 DNS 预获取，以帮助缩短页面加载时间。
seo-description: 对不同的解决方案和服务实施 DNS 预获取，以帮助缩短页面加载时间。
seo-title: 将 DNS 预获取用于不同的解决方案和服务
solution: Experience Cloud
title: 将 DNS 预获取用于不同的解决方案和服务
uuid: 4220e223-e00e-46b1-8bde-52248913bea1
translation-type: tm+mt
source-git-commit: f7ec8bf6087a18be41c9efbf05f60e6cfd24e566

---


# 将 DNS 预获取用于不同的解决方案和服务

对不同的解决方案和服务实施 DNS 预获取，以帮助缩短页面加载时间。

## 了解 DNS 预获取 {#section_772BF9CB7C4141DE9B0355146E2CD962}

浏览器使用DNS预取将网页上链接的域名自动解析为相应的IP地址。 预取过程开始浏览器加载网页时。 例如，假设您的页面中包含可单击的 `www.adobe.com` 链接。When a browser loads this page, it uses the [DNS system](https://www.networksolutions.com/support/what-is-a-domain-name-server-dns-and-how-does-it-work/) to look up the linked domain name and resolve it to a corresponding numeric IP address. DNS预取有助于提高页面性能，因为在站点访客单击该链接或按钮之前，域名已解析为IP地址。 DNS预取过程对用户是透明的。

## DNS 预获取和 Adobe Experience Cloud 解决方案 {#section_202A07F9F79F4ABDA44B98BA1DDCD516}

DNS预取可自动与页面上的静态、嵌入链接配合使用。 这也意味着自动DNS预取不适用于不同的 [!UICONTROL Experience Cloud解决方案和服务] ，因为：

* 每个Experience Cloud解决方案或服务在页面加载时动态生成DNS调用。
* 在进行这些调用之前，浏览器无法将域名解析为IP地址。

但是，您可以使用Experience Cloud解决方案手动实施DNS预取。 要执行此操作，您需要将 HTML `<dns-prefetch>` 标记添加到页面代码的 `<head>` 部分，如下所示。正确实施后，DNS 预获取可使页面加载时间缩短数毫秒。

## DNS 预获取代码示例 {#section_E886F7B2861E48BA9EF3D8B3CE32B345}

下面的示例说明了如何对不同的 [!DNL Experience Cloud] 解决方案和服务执行 DNS 预获取调用。有些预获取调用需要使用您的 [!DNL Adobe] 组织 ID 或跟踪服务器信息。在这些示例中，*斜体*&#x200B;格式的代码表示变量占位符。您需要将这些代码替换为您自己的 [!DNL Adobe] 合作伙伴 ID、客户代码或跟踪服务器信息等。

* **Analytics:** `<link rel="dns-prefetch" href="//insert tracking server name here">`.

   如果您使用非安全或安全跟踪服务器，请为每个 DNS 名称添加单独的标记。

* **Audience Manager:** `<link rel="dns-prefetch" href="//dpm.demdex.net">`

* **Experience Cloud ID服务：** 在此 `<link rel="dns-prefetch" href="//fast. *`处插入合作伙伴ID`*.demdex.net">`

* **Dynamic Tag Manager** (DTM)：不需要。当页面开始加载时，即可使用 DTM 链接。

* **Media Optimizer (Ad Cloud)：**

   * `<link rel="dns-prefetch" href="//pixel.everesttech.net">`
   * `<link rel="dns-prefetch" href="//cm.everesttechnet">`


* **[!DNL Target]:**`<link rel="dns-prefetch" href="//insert customer code here.tt.omtrdc.net">`

>[!MORE_LIKE_THIS]
>
>* [DNS预取](https://www.chromium.org/developers/design-documents/dns-prefetching)

