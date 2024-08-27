---
description: 了解如何对 Experience Cloud 中不同的应用程序和服务实施 DNS 预获取，以帮助缩短页面加载时间。
solution: Experience Cloud
title: 使用DNS预获取
uuid: 4220e223-e00e-46b1-8bde-52248913bea1
topic: Administration
role: Admin
level: Experienced
exl-id: caf2ff76-2076-436d-a5a7-aff531464480
source-git-commit: 2a80851c0a7d4ef7dbcc2565177b239f3e063164
workflow-type: tm+mt
source-wordcount: '346'
ht-degree: 91%

---

# 使用 DNS 预取

对不同的应用程序和服务实施 DNS 预获取，以帮助缩短页面加载时间。

## 了解 DNS 预获取

浏览器使用 DNS 预获取将网页上关联的域名自动解析为相应的 IP 地址。当您的浏览器加载网页时，会启动预获取过程。例如，假设您的页面中包含可选择的 `www.adobe.com` 链接。当浏览器加载此页面时，会使用 [DNS 系统](https://www.networksolutions.com/support/what-is-a-domain-name-server-dns-and-how-does-it-work/)查找关联的域名，并将其解析为相应的数字 IP 地址。DNS 预获取有助于提高页面性能，因为在网站访客单击该链接或按钮之前，系统已将域名解析为 IP 地址。DNS 预获取过程对用户是透明的。

## DNS 预获取和 Adobe Experience Cloud 应用程序

DNS 预获取会自动处理页面上的静态嵌入式链接。这也意味着自动DNS预获取不能与其他[!UICONTROL Experience Cloud]应用程序和服务一起使用，因为：

* 每个 Experience Cloud 应用程序或服务会在页面加载时动态生成 DNS 调用。
* 在生成这些调用之前，浏览器无法将域名解析为 IP 地址。

但是，您可以在 Experience Cloud 应用程序中手动实施 DNS 预获取。要执行此操作，您需要将 HTML `<dns-prefetch>` 标记添加到页面代码的 `<head>` 部分，如下所示。正确实施后，DNS 预获取可使页面加载时间缩短数毫秒。

## DNS 预获取代码示例

下面的示例说明了如何对不同的 [!DNL Experience Cloud] 应用程序和服务执行 DNS 预获取调用。有些预获取调用需要使用您的 [!DNL Adobe] 组织 ID 或跟踪服务器信息。在这些示例中，*斜体*&#x200B;格式的代码表示变量占位符。您需要将这些代码替换为您自己的 [!DNL Adobe] 合作伙伴 ID、客户代码或跟踪服务器信息等。

* **Analytics:** `<link rel="dns-prefetch" href="//data.example.com">`.

  如果您使用非安全或安全跟踪服务器，请为每个 DNS 名称添加单独的标记。

* **Audience Manager:** `<link rel="dns-prefetch" href="//dpm.demdex.net">`

* **Experience CloudID服务：** `<link rel="dns-prefetch" href="//fast.examplepartnerid.demdex.net">`

* **Advertising Cloud：**

   * `<link rel="dns-prefetch" href="//pixel.everesttech.net">`
   * `<link rel="dns-prefetch" href="//cm.everesttech.net">`

* **[!DNL Target]：**`<link rel="dns-prefetch" href="//example.tt.omtrdc.net">`

>[!MORELIKETHIS]
>
>* Chromium上的[DNS预获取](https://www.chromium.org/developers/design-documents/dns-prefetching)
