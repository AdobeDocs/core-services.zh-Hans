---
title: 通过CDN路由数据收集
description: 了解如何配置内容分发网络(CDN)，以便在不影响数据质量的情况下将数据收集请求转发到Adobe。
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
source-git-commit: e1185eeafc809b036b10955880536db7a576ca0b
workflow-type: tm+mt
source-wordcount: '1421'
ht-degree: 0%
---
# 通过CDN路由数据收集

某些组织通过其内容交付网络(CDN)路由数据收集请求，而不是将其直接发送到Adobe。 常见原因包括Web应用程序防火墙(WAF)保护、要求所有网站流量都必须通过CDN的公司政策，以及检查发送到Adobe的流量的功能。 CDN接收有关贵组织拥有的主机名的请求，然后将请求转发到名为源的Adobe数据收集主机名。

>[!IMPORTANT]
>
>Adobe无法查看或验证您的CDN配置。 贵组织和CDN提供商负责正确配置CDN。 要获取配置CDN的帮助，请与您的CDN提供商联系。 配置错误的CDN可能会导致数据丢失。

## 选择来源类型 {#origin-type}

| | 第三方来源（推荐） | 第一方来源 |
| --- | --- | --- |
| **原始主机名** | `data.adobedc.net`的租户ID子域，如`example.data.adobedc.net` | 您的第一方主机名，如`data.example.com` |
| Adobe服务器上的&#x200B;**证书** | Adobe的证书(`*.data.adobedc.net`) | [客户管理的证书](customer-managed-cert.md) |
| **证书续订** | 无需任何设置 | 贵组织在每次过期前续订证书并将其提供给Adobe |
| **区域锁定的[RDC](rdc.md)** | 不受支持 | 受支持 |
| **何时使用** | 所有CDN实施，除非您的组织需要第一方来源 | 您的安全策略要求直接控制原始证书，或者您的组织要求使用区域锁定的RDC类型 |

>[!NOTE]
>
>[Adobe管理的证书计划](adobe-managed-cert.md)不支持CDN实现。 Adobe无法验证域所有权或续订指向您的CDN的主机名的证书。 使用第三方来源或具有[客户管理的证书](customer-managed-cert.md)的第一方来源。

## 所有CDN实施的要求 {#requirements}

Adobe数据收集库，例如AppMeasurement和Web SDK，包含Adobe在每个请求中所需的一切。 配置您的CDN以将这些请求转发到Adobe而不更改它们。

>[!IMPORTANT]
>
>切勿更改端点或决定数据流向的任何内容，包括报表包ID (AppMeasurement)或数据流ID (Web SDK)。 更改这些值会导致数据丢失。

您的CDN配置必须：

* 转发请求方法、URL路径、查询字符串和正文，而不做更改。
* 保留`Host`标头不变。
* 将Adobe Cookie所在的域保持不变。
* 将所有Cookie保留在本指南的[Cookie部分](cookies/overview.md)中。
* 添加包含访客IP地址的`X-Forwarded-For`标头。 Adobe使用此标头进行地理定位。 如果没有该功能，地理位置数据将反映CDN服务器的位置，而不是访客的位置。
* 将Adobe的响应返回浏览器，而不进行更改。

您的CDN配置可以：

* 删除Adobe未使用的Cookie，例如网站上其他系统的Cookie。 不相关的Cookie会增加每个请求的开销。
* 使用WAF、机器人过滤或个人数据删除服务，只要它们不更改上面列出的任何内容。 在将这些服务应用于生产流量之前，请使用开发报表包或数据流测试这些服务。 过于激进的筛选可能会删除足够的数据，导致报表不可用。

您的CDN配置不能：

* 缓存数据收集请求或响应。 每次请求都必须发送到Adobe。
* 指向不存在的原始主机名。
* 接受过期的证书或固定来自源的特定证书。 Adobe不支持提供过期的证书，可以随时删除它们。

## 使用第三方源配置CDN {#third-party-origin}

第三方源使用Adobe自己的证书，因此您的组织不需要在Adobe服务器上维护证书。

1. 查找您组织的租户ID。 查看[查找您的租户ID](collection-domain.md#tenant-id)。
1. 在您的CDN配置中，将原始主机名设置为`data.adobedc.net`的租户ID子域。 例如：`example.data.adobedc.net`。
1. 为源启用服务器名称指示(SNI)。 将SNI主机名设置为原始主机名（例如，`example.data.adobedc.net`），而不是您网站的主机名。
1. 配置CDN以满足以上所有CDN实施[的要求](#requirements)。
1. 如果实施发送更改数据的主机名，请[更新实施](collection-domain.md#update-implementation)。 如果保留相同的主机名，则不需要更改实施。

>[!WARNING]
>
>请勿将您的来源设置为Adobe作为CNAME目标提供的主机名，如`hiodsibxvip01.data.adobedc.net`。 该主机名会绑定到您的第一方证书，并且在删除证书时可能会停止工作。

第三方源始终使用默认的[RDC类型](rdc.md)，因此可以在任何Adobe数据收集位置收集数据。

## 使用第一方源配置CDN {#first-party-origin}

仅在贵组织需要第一方来源时才使用。 常见原因包括：

* 您的安全策略要求直接控制原始证书。 例如，您的组织必须能够通过自己的证书颁发机构撤销证书。
* 您的组织需要区域锁定的[RDC类型](rdc.md)。

1. 请联系Adobe客户关怀部门，为您的第一方主机名（如`data.example.com`）设置[客户管理的证书](customer-managed-cert.md)。 如果您的组织需要区域锁定的RDC类型，请在请求中指定该类型。
1. 在您的CDN配置中，将原始主机名设置为您的第一方主机名。
1. 为源启用服务器名称指示(SNI)。 将SNI主机名设置为您的第一方主机名，并配置您的CDN以期望您的第一方证书来自来源。
1. 配置CDN以满足以上所有CDN实施[的要求](#requirements)。
1. 如果实施发送更改数据的主机名，请[更新实施](collection-domain.md#update-implementation)。 如果保留相同的主机名，则不需要更改实施。

>[!IMPORTANT]
>
>贵组织负责续订客户管理的证书，并在证书过期前将其提供给Adobe客户关怀团队。 如果Adobe服务器上的证书过期，则您的CDN可以在不通知您的情况下拒绝连接并丢弃数据。 请参阅[续订证书](customer-managed-cert.md#renewals)。

## 将现有的第一方实施移至CDN {#migrate}

如果您的组织当前使用Adobe托管的证书将数据直接发送到第一方主机名，请使用以下步骤迁移到CDN：

1. 识别在所有Adobe产品中向您的第一方主机名发送数据的每个实施。 其他产品（如Adobe Target或Adobe Journey Optimizer）可能会使用相同的主机名，并且单个证书可以覆盖多个主机名。
1. 选择[原始类型](#origin-type)。 如果您选择第一方来源，请联系Adobe客户关怀团队，以将您的证书转换为[客户管理的证书](customer-managed-cert.md)，使其过期。
1. 配置您的CDN。 保留现有主机名，以便您无需更新实施。
1. 在证书过期之前，将您的主机名指向您的CDN并切换所有实施以使用它。
1. [检查您的数据](#check)。
1. 如果您选择了第三方来源，请联系Adobe客户关怀团队，将您的第一方证书标记为待删除。

一旦您的主机名指向您的CDN，Adobe就无法续订您的第一方证书。 如果任何实施在证书过期时仍依赖证书，则该实施中的数据将丢失。 联系Adobe客户关怀团队可让您的组织控制何时移除证书。

## 检查您的数据 {#check}

Adobe无法验证您的CDN配置。 通过CDN路由数据收集后，比较更改之前和更改之后的数据：

* 数据继续以正常的卷到达预期的报表包、数据流或数据集。
* 地理位置报表显示访客的位置，而不是CDN服务器所在的少数城市。
* 独特访客计数不会意外增加。
* 在浏览器的开发人员工具中，对主机名的数据收集请求成功，并且Adobe Cookie与之前设置在同一域中。

## 常见配置错误

已知以下问题会导致数据质量问题或数据丢失。 这份清单并非详尽无遗。

| 症状 | 可能的原因 |
| --- | --- |
| 数据停止到达报表包或数据流 | CDN会更改请求URL，或者原始主机名不存在 |
| 证书过期后，数据将停止到达 | CDN需要来自源的第一方证书，并且该证书已过期 |
| 地理位置数据只显示几个城市 | CDN未添加`X-Forwarded-For`标头 |
| 独特访客计数意外增加 | CDN将删除Adobe Cookie、更改`Host`标头或更改Cookie域 |
| 报表缺少大量数据 | 个人数据删除或WAF规则删除的每个请求过多 |

## 常见问题

+++本页是否适用于Adobe Analytics以外的产品？

是的。 本页适用于所有使用Adobe数据收集的Adobe产品，包括Customer Journey Analytics、Adobe Experience Platform、Adobe Target和Adobe Journey Optimizer。

+++

+++Adobe是否可以拒绝不通过我的CDN的数据？

没有。 Adobe当前不提供将数据收集限制为来自CDN的请求的方法。

+++

+++Adobe能否提供或验证我的CDN的配置？

没有。 CDN配置选项因提供商而异，并且会随着时间的推移而改变。 请与您的CDN提供商联系，以获得配置CDN的帮助，并参阅[检查您的数据](#check)以了解识别配置问题的方式。

+++
