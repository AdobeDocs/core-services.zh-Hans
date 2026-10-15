---
title: 选择数据收集域
description: 了解可用于将数据发送到Adobe的域，以及如何查找贵组织的租户ID。
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
  - id: d3cdead0-685a-4489-9250-4bb709942f66
    internal-label: Data collection
source-git-commit: e1185eeafc809b036b10955880536db7a576ca0b
workflow-type: tm+mt
source-wordcount: '623'
ht-degree: 3%
---
# 选择数据收集域

您的数据收集域是您的实施将数据发送到的主机名。 所有使用Adobe数据收集的Adobe CX Enterprise产品（例如Adobe Analytics、Customer Journey Analytics、Adobe Experience Platform、Adobe Target和Adobe Journey Optimizer）都依赖于此域。

## 数据收集域选项

| 选项 | 实施域 | 区域锁定的[RDC](rdc.md) | 证书维护 |
| --- | --- | --- | --- |
| [第三方域](#third-party) | `example.data.adobedc.net` | 不受支持 | 无 |
| 具有[Adobe托管证书](adobe-managed-cert.md)的第一方域 | `data.example.com` | 受支持 | 无（Adobe自动续订证书） |
| 具有[客户管理的证书](customer-managed-cert.md)的第一方域 | `data.example.com` | 受支持 | 您的组织会续订证书并将其提供给Adobe |
| [具有第三方来源的内容交付网络(CDN)](cdn.md#third-party-origin) | `data.example.com` | 不受支持 | 无 |
| 具有第一方来源的[CDN](cdn.md#first-party-origin) | `data.example.com` | 受支持 | 您的组织会续订证书并将其提供给Adobe |

## 第三方数据收集域 {#third-party}

如果您不使用第一方域，请将数据发送到`data.adobedc.net`的子域。 Adobe建议使用您组织的[租户ID](#tenant-id)作为子域。 例如：`example.data.adobedc.net`。 当您[通过CDN](cdn.md)路由数据收集时，此域也是推荐的来源。

* 第三方域始终使用默认[RDC类型](rdc.md#third-party-data-collection)。
* 请勿使用比`example.data.adobedc.net`更深的子域。 例如，`custom.example.data.adobedc.net`不是有效的数据收集域。
* 较旧的实施可能使用诸如`sc.omtrdc.net`或`2o7.net`之类的域。 虽然这些域仍然有效，但Adobe建议尽可能使用`data.adobedc.net`。

### 查找您的租户ID {#tenant-id}

1. 使用您的Adobe ID凭据登录[Adobe CX Enterprise](https://experience.adobe.com)。
1. 在CX Enterprise界面中的任意位置，按`[Cmd]` + `[I]` (macOS)或`[Ctrl]` + `[I]` (Windows)。
1. 出现&#x200B;**[!UICONTROL 用户数据调试器]**。 选择&#x200B;**[!UICONTROL 分配的组织]**&#x200B;选项卡。
1. 展开所需的IMS组织。
1. 找到&#x200B;**[!UICONTROL 租户]**&#x200B;字段。 此值是您的租户ID。

您的租户ID与以`@AdobeOrg`结尾的IMS组织ID不同。 每个IMS组织都有一个租户ID。 如果您的公司使用多个IMS组织，则每个组织都有自己的租户ID。

## 更新实施 {#update-implementation}

当您更改数据收集域时，请更新每个将数据发送到Adobe的实施：

* **Web SDK标记扩展**：配置该扩展时更新[[!UICONTROL Edge域]](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/configure/general)字段。
* **Web SDK (alloy)**：更新`configure`命令中的[`edgeDomain`](https://experienceleague.adobe.com/en/docs/experience-platform/collection/js/commands/configure/edgedomain)属性。
* **Adobe Analytics扩展**：配置扩展时更新[[!UICONTROL SSL跟踪服务器]](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/analytics/overview)字段。 确保您还安装了[访客ID服务标记扩展](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/id-service/overview)。 有关详细信息，请参阅使用Analytics标记扩展的[访客识别](https://experienceleague.adobe.com/en/docs/analytics/implementation/id/analytics-extension)。
* **AppMeasurement**：更新[`trackingServerSecure`](https://experienceleague.adobe.com/en/docs/analytics/implementation/vars/config-vars/trackingserversecure)配置变量。 确保您还使用`VisitorAPI.js`实施了[访客ID服务](https://experienceleague.adobe.com/zh-hans/docs/id-service/using/home)。 有关详细信息，请参阅使用AppMeasurement的[访客识别](https://experienceleague.adobe.com/en/docs/analytics/implementation/id/appmeasurement)。
* **其他实施**：更新向Adobe发送数据的任何其他实施中的数据收集域，例如移动应用或服务器端实施。

如果您的实施不使用访客ID服务或Web SDK，则更改您的数据收集域将更改访客Cookie的域，并且回访访客将计为新访客。

如果您的网站使用多种实施方法，并且您无法同时更新所有方法，请考虑配置一个宽限期。 有关如何防止将访客计为网站上的新访客的其他步骤，请参阅[访客ID服务迁移注意事项](https://experienceleague.adobe.com/en/docs/analytics/implementation/id/migration)。
