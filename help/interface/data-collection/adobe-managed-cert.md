---
description: 了解如何设置安全证书以用于Adobe Experience Cloud第一方Cookie。
solution: Experience Cloud,Analytics
title: Adobe 管理的证书计划
index: y
snippet: y
feature: Cookies
topic: Administration
role: Admin
level: Experienced
exl-id: e15abde5-8027-4aed-a0c1-8a6fc248db5e
source-git-commit: 2a80851c0a7d4ef7dbcc2565177b239f3e063164
workflow-type: tm+mt
source-wordcount: '929'
ht-degree: 4%

---

# Adobe 管理的证书计划

Adobe管理的证书程序是用于设置CNAME实施所需的第一方证书的推荐流程。 程序在配置后是完全自动的。 它会及时更新证书，以便不会由于证书过期而影响数据收集。 您的前100个CNAME可以免费使用该程序。

如果您目前管理自己的证书，则需负责购买、维护证书并提供给Adobe以供第一方Cookie使用。 您可以联系Adobe客户关怀部门，讨论迁移到Adobe管理的证书计划事宜。

## 实施

请按照以下步骤为第一方数据收集实施新证书：

1. 下载并填写[第一方域请求表单](cookies/assets/First_Party_Domain_Request_Form.xlsx)

1. 通过Adobe客户关怀部门开立一个票证，请求根据Adobe管理的证书计划设置第一方数据收集。

1. Adobe代表在收到票证后会为您提供CNAME记录。 必须在贵公司的 DNS 服务器上配置这些记录，然后 Adobe 才能代表您购买证书。例如，主机名`data.example.com`指向`hiodsibxvip01.data.adobedc.net`。

1. 当CNAME记录位于您组织的服务器上时，Adobe会与DigiCert一起购买证书并安装到Adobe数据收集服务器上。

## 验证主机名转发 {#validate}

Adobe安装证书后，可以使用以下方法之一验证证书是否正常工作。

+++**浏览器验证**

您可以使用任意浏览器验证证书是否已正确安装。 在地址栏中键入包含`_check`作为路径的CNAME。 例如：

`data.example.com/_check`

如果一切正常，浏览器会显示`SUCCESS`。 如果证书安装不正确，您会收到安全警告。

+++

+++**命令行(`curl`)**

大多数现代操作系统已安装[`curl`](https://curl.se)。

在命令行中键入以下内容：

```sh
curl data.example.com/_check
```

如果一切工作正常，控制台将返回`SUCCESS`。

>[!TIP]
>
>您可以使用`-k`标记禁用安全警告以帮助进行故障排除。

+++

+++**命令行(`nslookup`)**

在命令行中键入以下内容：

```sh
nslookup data.example.com
```

如果一切工作正常，将返回Adobe的数据收集服务器：

```text
Server: hiodsibxvip01.corp.adobe.com
Address: 10.50.112.247

Name: example.com.ssl.d1.sc.omtrdc.net
Addresses: 63.140.37.126
    63.140.37.206
    63.140.36.51
    63.140.36.145
Aliases: smetrics.example.com
```

+++

## 更新实施代码 {#update}

在验证证书是否正确工作后，您可以更新Adobe实施以使用这些值。

* 对于Adobe AnalyticsAppMeasurement实施，请更新[`trackingServer`](https://experienceleague.adobe.com/zh-hans/docs/analytics/implementation/vars/config-vars/trackingserver)配置变量。 如果您已有实施，请参阅[访客迁移](https://experienceleague.adobe.com/zh-hans/docs/analytics/technotes/visitor-migration)，以了解有关如何防止将现有访客计为新访客的其他步骤。
* 对于Web SDK实施，更新[`configure`](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/web-sdk/commands/configure/overview)命令中的[`edgeDomain`](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/web-sdk/commands/configure/edgedomain)属性。

## 维护和续订

在第一方证书过期前三十天，Adobe将验证CNAME是否仍然有效并在使用中。 如果是，Adobe会假定您要继续使用该服务，并代表您自动续订证书。

>[!IMPORTANT]
>
>如果您组织的CNAME记录已被删除或不再映射到提供的Adobe安全主机名，则Adobe无法续订证书。 在Adobe系统中，该条目被标记为无需进一步通信即可删除。

## 常见问题解答

+++此过程是否安全？

可以。Adobe管理的证书计划比向Adobe提供证书的组织更安全。 证书或私钥不会在Adobe和证书颁发机构的外部易手。

+++

+++Adobe如何为我们的域购买证书？

仅当您将指定的主机名指向Adobe拥有的主机名时，才能购买证书。 您实际上会将此主机名委派给Adobe，并允许Adobe代表您购买证书。

+++

+++我可以请求吊销证书吗？

可以。作为域所有者，您有权请求吊销证书。 请联系Adobe客户关怀团队以启动此流程。

+++

+++使用哪种加密类型？

Adobe与DigiCert一起颁发SHA-2证书。

+++

+++此计划是否会产生额外费用？

不会。Adobe免费为所有Adobe Experience Cloud客户提供此服务。

+++

+++Adobe提供了哪些密码安全级别？

Adobe提供两种密码安全级别，以满足客户对第一方数据收集安全性的不同需求。 这些级别确定与Adobe服务器的HTTPS连接支持哪些加密算法。 Adobe会根据当前的安全实践定期审查和更新支持的算法集。 如果要更改密码安全设置，请联系客户关怀团队。

* **Standard**&#x200B;需要TLS 1.2或更高版本以及至少128位加密。 它旨在提供最广泛的设备兼容性，同时保持安全加密。
* **高**&#x200B;密码安全级别需要TLS 1.2或更高版本并移除对较弱密码的支持。 它专为希望获得最强加密并且不关心旧设备支持的客户而设计。

已知下列客户端无法连接密码安全设置为&#x200B;**高**：

* Windows 8.1及更早版本（最后更新于2018年）
* Windows Phone 8.1及更早版本（最后更新于2016年）
* OS X 10.10及更早版本（最后更新于2017年）
* iOS 8.4及更早版本（最后更新于2015年）

+++

+++支持哪些HTTPS证书类型？

Adobe同时支持RSA和ECC证书类型，以满足不同的客户需求。 客户端更广泛地支持RSA证书，但ECC证书在服务器和客户端使用的处理较少。 对于Adobe管理的证书，同时提供了RSA和ECC。 对于客户管理的证书，需要RSA，并且建议使用ECC。 新式客户端同时支持RSA和ECC。 以下客户端通常仅支持RSA证书：

* Windows Vista及更早版本（最后更新于2012年）
* Windows Phone 8.0及更早版本（最后更新于2014年）
* OS X 10.8及更早版本（最后更新于2013年）
* iOS 5.1及更早版本（最后更新于2012年）
* Android 4.3及更早版本（最后更新于2013年）

+++
