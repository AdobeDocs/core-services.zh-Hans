---
title: 客户管理的证书
description: 了解何时将客户管理的证书用于第一方数据收集，以及贵组织续订该证书的责任。
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
    internal-label: CX Enterprise
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: d378ca77-2da1-4f39-ad92-1917fe974a38
    internal-label: Experienced
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
    internal-label: Security
  - id: d3cdead0-685a-4489-9250-4bb709942f66
    internal-label: Data collection
source-git-commit: 18fd590d6f0fd1800e3d5c62851453aa91d9db5f
workflow-type: tm+mt
source-wordcount: '694'
ht-degree: 1%
---
# 客户管理的证书

使用客户管理的证书，贵组织会获取您第一方数据收集主机名的证书并将其提供给Adobe。 Adobe在其数据收集服务器上托管证书。 贵组织负责续订证书并在当前证书过期之前向Adobe提供每个续订的证书。

>[!TIP]
>
>对于大多数第一方实施，Adobe建议使用[Adobe管理的证书计划](adobe-managed-cert.md)。 这样更加安全，并且会自动更新证书。 仅在贵组织需要客户管理的证书时才使用它。

## 何时使用客户管理的证书

* **您通过具有第一方来源的CDN路由数据收集**： [Adobe管理的证书计划](adobe-managed-cert.md)不支持CDN实施。 请参阅[使用第一方源配置CDN](cdn.md#first-party-origin)。
* **您的安全策略要求直接控制证书**：例如，您的组织必须能够通过自己的证书颁发机构撤销证书，而不是通过Adobe客户关怀部门请求撤销。
* **您的组织需要特定的证书颁发机构或证书类型**： Adobe管理的证书程序使用DigiCert颁发的证书。

## 比较证书方法

| | Adobe 管理的证书 | 客户管理的证书 |
| --- | --- | --- |
| **谁正在获取证书** | Adobe，通过DigiCert | 您的组织，通过您选择的商业证书颁发机构 |
| **续订** | Adobe会自动续订证书 | 贵组织在每次过期前续订证书并将其提供给Adobe |
| **证书类型** | Adobe同时提供RSA和ECC证书 | 需要RSA ；建议使用ECC |
| CDN支持&#x200B;**&#x200B;** | 否 | 是，作为第一方来源 |

## 设置客户管理的证书

1. 请联系Adobe客户关怀部门，以使用客户管理的证书请求第一方数据收集。 包括您的第一方主机名，如`data.example.com`。 如果贵组织具有数据驻留或合规性要求，请在请求中指定所需的[RDC类型](rdc.md)。
1. Adobe客户关怀团队为您的主机名提供证书签名请求(CSR)。 Adobe会生成并保留私钥，这样您的组织永远不会处理私钥。 Adobe需要RSA证书并建议ECC证书。 每种证书类型都需要自己的CSR，因此如果您需要ECC证书，请向Adobe客户关怀团队索取ECC CSR。
1. 将每个CSR提交到所需的商业证书颁发机构，以获取已签名的证书。 不支持免费证书服务。 按照客户关怀部门的指示，向Adobe提供已颁发的证书。
1. Adobe安装证书后，会将主机名的流量定向到Adobe：
   * **没有CDN**：按照Adobe客户关怀部门的指示更新组织的DNS记录。
   * 使用CDN **&#x200B;**：将您的CDN源设置为第一方主机名。 请参阅[使用第一方源配置CDN](cdn.md#first-party-origin)。
1. 如果您的实施尚未将数据发送到此主机名，请[更新您的实施](collection-domain.md#update-implementation)。

## 续订您的证书 {#renewals}

贵组织有责任在当前证书过期之前续订证书并将续订证书提供给Adobe客户关怀团队。

如果Adobe服务器上的证书过期，则浏览器和CDN会拒绝与您的主机名的连接，并且来自这些请求的数据将丢失。 CDN无需通知您即可丢弃此数据。

最大证书生命周期正在缩短，这使得续订更加频繁。 有关详细信息，请参阅CA/Browser论坛服务器证书基线要求中的[6.3.2证书操作期和密钥对使用期](https://cabforum.org/working-groups/server/baseline-requirements/requirements/#632-certificate-operational-periods-and-key-pair-usage-periods)。 要避免数据收集出现缺口，请执行以下操作：

* 跟踪您向Adobe提供的每个证书的过期日期。
* 为续订分配责任人，并记录续订流程，以便在员工更改时继续进行。

Adobe目前正在探索自助服务证书续订流程。

## 停止使用客户管理的证书

* **要移至Adobe管理的证书计划**：请与Adobe客户关怀部门联系。 Adobe管理的证书计划要求您的主机名直接指向Adobe，而不是CDN。
* **停止使用第一方主机名**：更新使用该主机名的所有实施，然后联系Adobe客户关怀部门以从Adobe服务器中删除证书。
* **要移动到具有第三方来源的CDN**：请参阅[将现有的第一方实现移动到CDN](cdn.md#migrate)。
