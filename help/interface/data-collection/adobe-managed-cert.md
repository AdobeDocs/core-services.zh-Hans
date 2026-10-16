---
description: 了解如何设置安全证书以用于Adobe CX Enterprise第一方Cookie。
solution: Experience Cloud,Analytics
title: Adobe 管理的证书计划
index: true
snippet: 'y'
feature: Cookies
topic: Administration
role: Admin
level: Experienced
exl-id: e15abde5-8027-4aed-a0c1-8a6fc248db5e
autotag-review: '2026-09-09T20:12:24.943Z'
TQID: 'https://experienceleague.adobe.com/8CSBLQaw3KOByyxxCYr1By4gyAQsDIhiofOdAzn38dg'
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
    internal-label: CX Enterprise
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
    internal-label: Metrics
  - id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
    internal-label: Implementations
  - id: fd307ce7-56f5-4ee3-af68-a7833ff6e85e
    internal-label: API
  - id: fdbb8fc9-ffa3-4b86-88fe-aa4c5a3e1bc6
    internal-label: Administration
subfeature_v2:
  - id: b75843fa-0a67-4a44-a6b1-cc627b0481dc
    internal-label: Support
  - id: c8add8f2-4250-4fd9-9cde-9707036c567d
    internal-label: Methods
  - id: d2311670-43bd-4c2e-bc98-1da2aaba9cef
    internal-label: Appmeasurement implementation
  - id: e992d880-33bc-4949-a648-aa7d410276cd
    internal-label: Validation
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: d378ca77-2da1-4f39-ad92-1917fe974a38
    internal-label: Experienced
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
    internal-label: Measurement
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
    internal-label: Security
  - id: d3cdead0-685a-4489-9250-4bb709942f66
    internal-label: Data collection
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: 18fd590d6f0fd1800e3d5c62851453aa91d9db5f
workflow-type: tm+mt
source-wordcount: '1055'
ht-degree: 2%
---
# Adobe 管理的证书计划

Adobe管理的证书计划是用于设置CNAME实施所需的第一方证书的推荐流程。 程序在配置后是完全自动的。 它会及时更新证书，以便不会由于证书过期而影响数据收集。 您的前100个CNAME可以免费使用该程序。

Adobe管理的证书计划不支持通过内容交付网络(CDN)路由收集数据。 如果您使用CDN，请参阅[通过CDN路由数据收集](cdn.md)。 需要管理自己的证书的组织可以改用[客户管理的证书](customer-managed-cert.md)。 如果您当前管理自己的证书，并且希望转到Adobe管理的证书计划，请联系Adobe客户关怀团队。

## 实施

要实施用于第一方数据收集的新证书，请执行以下步骤：

1. 下载并填写[第一方域请求表单](cookies/assets/First_Party_Domain_Request_Form.xlsx)
1. 向Adobe客户关怀部门开立一个票证，请求根据Adobe管理的证书计划设置第一方数据收集。 如果贵组织具有数据驻留或合规性要求，请在请求中指定所需的[RDC类型](rdc.md)。
1. 在收到票证后，Adobe代表会为您提供一个CNAME记录。 您必须在贵公司的DNS服务器上配置此记录，然后Adobe才能代表您购买证书。 例如，主机名`data.example.com`指向`hiodsibxvip01.data.adobedc.net`。 如果贵组织使用DNS证书颁发机构授权(CAA)记录，请确保您的CAA记录允许DigiCert颁发证书。 请参阅[维护和续订](#renewals)。
1. 当CNAME记录位于您组织的服务器上时，Adobe会与DigiCert一起购买证书并安装到Adobe数据收集服务器上。
1. 如果您在由Adobe CNAME托管时出于第一方目的需要更新`robots.txt`文件，请联系客户关怀团队提出请求。 当您想要更新`robots.txt`文件以阻止抓取您的子域时，此类请求相关。

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

要使用新的CNAME主机名，请在验证证书是否正确工作之后更新您的Adobe实施。 请参阅[更新您的实施](collection-domain.md#update-implementation)。

## 维护和续订 {#renewals}

Adobe会自动续订您的证书。 在证书过期前三十天，Adobe将验证CNAME是否仍然有效且正在使用中，然后代表您续订证书。 要保持续订有效，请避免以下DNS更改：

* **删除或重新指向CNAME记录**：如果CNAME记录被删除或不再指向Adobe安全主机名，Adobe无法续订证书。 此条件包括将CNAME记录指向内容交付网络(CDN)。 如果您计划使用CDN，请参阅[在更改DNS记录之前，将现有的第一方实施移动到CDN](cdn.md#migrate)。
* **添加不授权DigiCert的CAA记录**：证书颁发机构检查主机名及其父域上的证书颁发机构授权(CAA)记录。 如果使用CAA记录，请将`digicert.com`作为授权颁发者加入。 例如：`example.com. IN CAA 0 issue "digicert.com"`。
* **将DigiCert发布限制到特定帐户**： DigiCert的域锁定功能向CAA记录添加`account=`参数，如`example.com. IN CAA 0 issue "digicert.com; account=<token>"`。 此参数限制向组织的DigiCert帐户颁发，即使`digicert.com`获得授权，也会阻止Adobe获取证书。 如果您的组织需要DigiCert域锁定，请改用[客户管理的证书](customer-managed-cert.md)。 在域注册机构中设置的域锁（有时称为传输锁）不相关，不会影响Adobe管理的证书。

>[!IMPORTANT]
>
>如果您的CNAME记录不再指向Adobe安全主机名，则Adobe系统中的条目将标记为删除，且不会进行进一步通信。

## 常见问题

+++此过程是否安全？

可以。 Adobe管理的证书程序比[客户管理的证书](customer-managed-cert.md)更安全。 在Adobe和证书颁发机构之外不传输证书或私钥。

+++

+++Adobe如何为我们的域购买证书？

仅当您将指定的主机名指向Adobe拥有的主机名时，才能购买证书。 您可以将此主机名委派给Adobe，并允许Adobe代表您购买证书。

+++

+++我可以请求吊销证书吗？

可以。 作为域所有者，您有权请求吊销证书。 请联系Adobe客户关怀团队以启动此流程。

+++

+++使用哪种加密类型？

Adobe与DigiCert一起颁发SHA-2证书。

+++

+++此计划是否会产生额外费用？

对于前100个CNAME，Adobe会向所有Adobe CX Enterprise客户提供此计划，而不需要支付额外费用。

+++

+++Adobe提供了哪些密码安全级别？

Adobe提供两种密码安全级别，以满足客户对第一方数据收集安全性的不同需求。 这些级别确定与Adobe服务器的HTTPS连接支持哪些加密算法。 Adobe会根据当前的安全实践定期审查和更新支持的算法集。 要更改密码安全设置，请联系客户关怀团队。

* **Standard**&#x200B;需要TLS 1.2或更高版本以及至少128位加密。 它旨在提供最广泛的设备兼容性，同时保持安全加密。
* **高**&#x200B;需要TLS 1.2或更高版本并移除对较弱密码的支持。 它专为需要最强加密功能的客户而设计。 在2015年之前发布的客户端通常在密码安全设置为&#x200B;**高**&#x200B;时无法连接。

+++

+++支持哪些HTTPS证书类型？

Adobe同时支持RSA和ECC证书，并且新式客户端同时支持这两种证书类型。 ECC证书在服务器和客户端上所需的处理资源较少。 对于Adobe管理的证书，Adobe同时提供RSA和ECC证书。 对于[客户管理的证书](customer-managed-cert.md)，需要RSA，建议使用ECC。

+++

