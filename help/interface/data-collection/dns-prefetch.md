---
description: 了解如何对CX Enterprise中不同的应用程序和服务实施DNS预获取，以帮助缩短页面加载时间。
solution: Experience Cloud
title: 使用DNS预获取
uuid: 4220e223-e00e-46b1-8bde-52248913bea1
topic: Administration
role: Admin
level: Experienced
exl-id: caf2ff76-2076-436d-a5a7-aff531464480
TQID: https://experienceleague.adobe.com/oAe81mw-qFetDM0zky2eS6DNf-XZ67H68Qw-Sa8mk0Y
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
feature_v2:
  - id: fdbb8fc9-ffa3-4b86-88fe-aa4c5a3e1bc6
subfeature_v2:
  - id: b75843fa-0a67-4a44-a6b1-cc627b0481dc
  - id: fef08361-6ac5-460c-93fe-d063e40b6a49
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 50012e2564e88e1a6e16578e3331136c7df0cb21
workflow-type: tm+mt
source-wordcount: 350
ht-degree: 77%

---

# 使用 DNS 预取

对不同的应用程序和服务实施 DNS 预获取，以帮助缩短页面加载时间。

## 了解 DNS 预获取

浏览器使用 DNS 预获取将网页上关联的域名自动解析为相应的 IP 地址。 当您的浏览器加载网页时，会启动预获取过程。 例如，假设您的页面中包含可选择的 `www.adobe.com` 链接。 当浏览器加载此页面时，会使用 _DNS 系统_&#x200B;查找关联的域名，并将其解析为相应的数字 IP 地址。 DNS 预获取有助于提高页面性能，因为在网站访客单击该链接或按钮之前，系统已将域名解析为 IP 地址。 DNS 预获取过程对用户是透明的。

## DNS预获取和Adobe CX Enterprise应用程序

DNS 预获取会自动处理页面上的静态嵌入式链接。 这也意味着自动DNS预获取不能与其他[!UICONTROL CX Enterprise]应用程序和服务结合使用，因为：

* 每个CX Enterprise应用程序或服务会在页面加载时动态生成DNS调用。
* 在生成这些调用之前，浏览器无法将域名解析为 IP 地址。

但是，您可以在CX Enterprise应用程序中手动实施DNS预获取。 要执行此操作，您需要将 HTML `<dns-prefetch>` 标记添加到页面代码的 `<head>` 部分，如下所示。 正确实施后，DNS 预获取可使页面加载时间缩短数毫秒。

## DNS 预获取代码示例

下面的示例说明了如何对不同的 [!DNL CX Enterprise] 应用程序和服务执行 DNS 预获取调用。 有些预获取调用需要使用您的 [!DNL Adobe] 组织 ID 或跟踪服务器信息。 在这些示例中，*斜体*&#x200B;格式的代码表示变量占位符。 您需要将这些代码替换为您自己的 [!DNL Adobe] 合作伙伴 ID、客户代码或跟踪服务器信息等。

* **Analytics:** `<link rel="dns-prefetch" href="//data.example.com">`.

  如果您使用非安全或安全跟踪服务器，请为每个 DNS 名称添加单独的标记。

* **Audience Manager:** `<link rel="dns-prefetch" href="//dpm.demdex.net">`

* **CX Enterprise ID服务：** `<link rel="dns-prefetch" href="//fast.examplepartnerid.demdex.net">`

* **Advertising Cloud：**

   * `<link rel="dns-prefetch" href="//pixel.everesttech.net">`
   * `<link rel="dns-prefetch" href="//cm.everesttech.net">`

* **[!DNL Target]:** `<link rel="dns-prefetch" href="//example.tt.omtrdc.net">`

>[!MORELIKETHIS]
>
>* Chromium上的[DNS预获取](https://www.chromium.org/developers/design-documents/dns-prefetching)

