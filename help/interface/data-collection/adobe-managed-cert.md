---
description: 了解如何设置安全证书以用于Adobe CX Enterprise第一方Cookie。
solution: Experience Cloud,Analytics
title: Adobe 管理的证书计划
index: true
snippet: y
feature: Cookies
topic: Administration
role: Admin
level: Experienced
exl-id: e15abde5-8027-4aed-a0c1-8a6fc248db5e
TQID: https://experienceleague.adobe.com/LWbjh-jXKmY6mcl047uzA1ZkhZlAmeNpt9JRg3Ynt9E
product_v2: id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b3f03848-ae12-48b2-8aab-cad18567eb32id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7aid: fdbb8fc9-ffa3-4b86-88fe-aa4c5a3e1bc6
subfeature_v2: id: b75843fa-0a67-4a44-a6b1-cc627b0481dcid: c8add8f2-4250-4fd9-9cde-9707036c567did: d2311670-43bd-4c2e-bc98-1da2aaba9cefid: e992d880-33bc-4949-a648-aa7d410276cdid: fef08361-6ac5-460c-93fe-d063e40b6a49
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: c1579802-ddd4-4214-8a91-97b2066abe11id: c2be0313-b3ae-45e0-b454-d20bf54b23f2id: d095671a-1355-40aa-8b5f-06c33c68080bid: d3cdead0-685a-4489-9250-4bb709942f66id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 50012e2564e88e1a6e16578e3331136c7df0cb21
workflow-type: tm+mt
source-wordcount: 1248
ht-degree: 2%

---

# Adobe 管理的证书计划

Adobe管理的证书计划是用于设置CNAME实施所需的第一方证书的推荐流程。 程序在配置后是完全自动的。 它会及时更新证书，以便不会由于证书过期而影响数据收集。 您的前100个CNAME可以免费使用该程序。

如果您目前管理自己的证书，则需负责购买、维护证书并将证书提供给Adobe以供第一方Cookie使用。 您可以联系Adobe客户关怀部门，讨论迁移到Adobe管理的证书计划的问题。

## 实施

请按照以下步骤为第一方数据收集实施新证书：

1. 下载并填写[第一方域请求表单](cookies/assets/First_Party_Domain_Request_Form.xlsx)
1. 向Adobe客户关怀部门开立一个票证，请求根据Adobe管理的证书计划设置第一方数据收集。 如果贵组织具有数据驻留或合规性要求，请在请求中指定所需的[RDC类型](rdc.md)。
1. 在收到票证后，Adobe代表会为您提供一个CNAME记录。 您必须在贵公司的DNS服务器上配置此记录，然后Adobe才能代表您购买证书。 例如，主机名`data.example.com`指向`hiodsibxvip01.data.adobedc.net`。
1. 当CNAME记录位于您组织的服务器上时，Adobe会与DigiCert一起购买证书并安装到Adobe数据收集服务器上。

## 验证主机名转发

Adobe安装证书后，您可以使用以下方法之一来验证证书是否正常工作。

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
Aliases: data.example.com
```

+++

## 更新实施代码

在验证证书是否正确工作后，您可以更新Adobe实施以使用新的CNAME主机名。

* **Web SDK标记扩展**：配置该扩展时更新[[!UICONTROL Edge域]](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/configure/general)字段。
* **Web SDK (alloy)**：更新`configure`命令中的[`edgeDomain`](https://experienceleague.adobe.com/en/docs/experience-platform/collection/js/commands/configure/edgedomain)属性。
* **Adobe Analytics扩展**：配置扩展时更新[[!UICONTROL SSL跟踪服务器]](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/analytics/overview)字段。 确保您还安装了[访客ID服务标记扩展](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/id-service/overview)。 有关详细信息，请参阅使用Analytics标记扩展的[访客识别](https://experienceleague.adobe.com/en/docs/analytics/implementation/id/analytics-extension)。
* **AppMeasurement**：更新[`trackingServerSecure`](https://experienceleague.adobe.com/en/docs/analytics/implementation/vars/config-vars/trackingserversecure)配置变量。 确保您还使用`VisitorAPI.js`实施了[访客ID服务](https://experienceleague.adobe.com/zh-hans/docs/id-service/using/home)。 有关详细信息，请参阅使用AppMeasurement的[访客识别](https://experienceleague.adobe.com/en/docs/analytics/implementation/id/appmeasurement)。

如果您的网站使用多种实施方法，并且您无法同时更新所有方法，请考虑配置一个宽限期。 有关如何防止将访客计为网站上的新访客的其他步骤，请参阅[访客ID服务迁移注意事项](https://experienceleague.adobe.com/en/docs/analytics/implementation/id/migration)。

## 维护和续订

在第一方证书过期前三十天，Adobe会验证CNAME是否仍然有效并在使用中。 在这种情况下，Adobe会假定您要继续使用该服务，并代表您自动续订证书。

>[!IMPORTANT]
>
>如果您组织的CNAME记录被删除或不再映射到提供的Adobe安全主机名，Adobe将无法续订证书。 Adobe系统中的条目已标记为删除，无需进一步通信。

## 常见问题

+++此过程是否安全？

可以。 Adobe管理的证书计划比贵组织向Adobe提供证书更安全。 证书或私钥不会在Adobe和证书颁发机构的外部易手。

+++

+++Adobe如何为我们的域购买证书？

仅当您将指定的主机名指向Adobe拥有的主机名时，才能购买证书。 实际上，您可以将此主机名委派给Adobe，并允许Adobe代表您购买证书。

+++

+++我可以请求吊销证书吗？

可以。 作为域所有者，您有权请求吊销证书。 请联系Adobe客户关怀团队以启动此流程。

+++

+++使用哪种加密类型？

Adobe与DigiCert一起颁发SHA-2证书。

+++

+++此计划是否会产生额外费用？

不是。 Adobe为所有Adobe CX Enterprise客户提供此服务，无需支付额外费用。

+++

+++Adobe提供了哪些密码安全级别？

Adobe提供两种密码安全级别，以满足客户对第一方数据收集安全性的不同需求。 这些级别确定与Adobe服务器的HTTPS连接支持哪些加密算法。 Adobe会根据当前的安全实践定期审查和更新支持的算法集。 如果要更改密码安全设置，请联系客户关怀团队。

* **Standard**&#x200B;需要TLS 1.2或更高版本以及至少128位加密。 它旨在提供最广泛的设备兼容性，同时保持安全加密。
* **高**&#x200B;需要TLS 1.2或更高版本并移除对较弱密码的支持。 它专为希望获得最强加密并且不关心旧设备支持的客户而设计。

已知下列客户端无法连接密码安全设置为&#x200B;**高**：

* Windows 8.1及更早版本（最后更新于2018年）
* Windows Phone 8.1及更早版本（最后更新于2016年）
* OS X 10.10及更早版本（最后更新于2017年）
* iOS 8.4及更早版本（最后更新于2015年）

+++

+++支持哪些HTTPS证书类型？

Adobe同时支持RSA和ECC证书类型，以满足不同的客户需求。 客户端更广泛地支持RSA证书，但ECC证书在服务器和客户端使用的处理较少。 对于Adobe管理的证书，同时提供RSA和ECC。 对于客户管理的证书，需要RSA，并且建议使用ECC。 新式客户端同时支持RSA和ECC。 以下客户端通常仅支持RSA证书：

* Windows Vista及更早版本（最后更新于2012年）
* Windows Phone 8.0及更早版本（最后更新于2014年）
* OS X 10.8及更早版本（最后更新于2013年）
* iOS 5.1及更早版本（最后更新于2012年）
* Android 4.3及更早版本（最后更新于2013年）

+++

+++我可以改为管理自己的证书吗？

可以。 但是，如果您管理自己的证书，则需负责续订您的证书，并在每次续订证书时将其提供给Adobe。 如果贵组织忘记及时续订证书，此过程的安全性会降低，并且可能会导致数据收集出现缺口。 Adobe建议使用托管的证书程序而不是自己管理证书，特别是考虑到TLS证书最大生命周期的缩短。 有关详细信息，请参阅CA/Browser论坛服务器证书基线要求中的[6.3.2证书操作期和密钥对使用期](https://cabforum.org/working-groups/server/baseline-requirements/requirements/#632-certificate-operational-periods-and-key-pair-usage-periods)。
+++

