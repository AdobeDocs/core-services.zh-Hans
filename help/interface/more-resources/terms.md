---
description: 了解Adobe产品和界面术语在CX企业版、Experience Cloud解决方案、Creative Cloud、Experience League和其他支持体验中的差异。
solution: Experience Cloud
title: 术语
feature-set: Experience Cloud Services
feature: Central Interface Components
topic: Administration
role: Admin
level: Experienced
exl-id: 3799f806-2794-43ab-9e70-06ee693871e7
product_v2: id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
feature_v2: id: fdbb8fc9-ffa3-4b86-88fe-aa4c5a3e1bc6
subfeature_v2: id: b75843fa-0a67-4a44-a6b1-cc627b0481dcid: bdea9bc8-5600-45db-b85e-d74bb59dfcffid: fef08361-6ac5-460c-93fe-d063e40b6a49
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dcid: eddd9b14-83bd-4ff4-9072-54a4a484abb7id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 504cdc98f97b744efa27d3c09cd69cf7f81412a4
workflow-type: tm+mt
source-wordcount: 692
ht-degree: 5%

---

# 术语

<!--
TQID: https://experienceleague.adobe.com/6wm7HcuAbaV1iV3AgN55dY5WR---BnMM7lJgN0HZDsk
-->

当同一字出现在不同的Adobe体验（ CX企业版、营销应用程序、设计应用程序或支持站点）中时，请使用此表。 它不是完整的术语表；有关深层定义，请参阅[Experience League](https://experienceleague.adobe.com)上的产品特定帮助。

| 术语 | 在CX Enterprise和本指南中 | Adobe的其他常见用法 |
| --- | --- | --- |
| **Adobe CX Enterprise** | 位于`experience.adobe.com`的统一Web体验，您可以在其中打开营销应用程序、设置首选项和通知，以及访问共享界面服务（例如，客户属性和[受众库](../services/audiences/overview.md)）。 以前称为&#x200B;*Adobe Experience Cloud*。 | 与&#x200B;**Adobe Experience Platform**&#x200B;的产品不同（客户数据基础架构、沙盒、数据集）。 不是&#x200B;**Adobe Creative Cloud**（设计和媒体应用）。 |
| **Adobe Experience Platform** | 将数据收集、身份或平台代理连接到解决方案时显示；某些导航搜索和AI功能受平台支持。 | 一个数据和编排平台。 当指的是CX Enterprise Shell或主页时，请不要使用“Experience Platform”。 |
| **Experience League** | 帮助和产品内链接向您发送有关Adobe解决方案的&#x200B;**文档**、**教程**、学习播放列表、发行说明和社区上下文的信息。 从[Experience League主页](https://experienceleague.adobe.com)开始。 | 补充&#x200B;**[Adobe帮助中心](https://helpx.adobe.com/support.html)**，该中心强调个人和团队的&#x200B;**帐户**、**计划**、**计费**、下载和跨产品故障诊断。 使用帮助中心执行密码重置、计划更改和类似任务；使用Experience League执行产品操作说明内容。 |
| **AI助手/代理AI** | 本指南的AI主题中所述的产品内助理和精心安排的代理；访问和点数取决于产品授权。 | 其他Adobe表面（例如，**Firefly**&#x200B;或&#x200B;**Express**）使用具有不同范围和策略的“AI”功能。 |
| **组织** | 您的&#x200B;**IMS组织**： CX Enterprise中的企业许可、用户目录、SSO和Admin Console管理的边界。 查看[组织和帐户关联](../administration/organizations.md)。 | 不是Analytics *报告包*、Target *属性*&#x200B;或Experience Platform *沙盒*（这些是产品特定的容器）。 |
| **管理控制台** | 用户、产品配置文件和标识的企业控制平面位于`adminconsole.adobe.com`；链接自CX Enterprise **管理**&#x200B;主题。 查看[用户和产品管理](../administration/admin-console.md)。 | 不同于每个应用程序内的&#x200B;**产品内管理员**（例如，Analytics管理工具或Journey Optimizer权限屏幕）。 |
| **产品配置文件** | Admin Console中的许可证包，用于授予对产品或功能的访问权限；用户必须属于配置文件才能获得权限。 请参阅[管理产品和轮廓](https://helpx.adobe.com/cn/enterprise/using/manage-products.html)。 | 不能与产品中的每个“工作区”、“容器”或“属性”名称互换；这些名称因解决方案而异。 |
| **帐户关联** | 将应用程序登录（例如，Analytics或Target凭据）连接到组织的Adobe ID，以便服务识别一个用户。 查看[组织和帐户关联](../administration/organizations.md)。 | 与&#x200B;**目录同步**、**SSO**&#x200B;或&#x200B;**联合**&#x200B;设置不同（这些是Admin Console中的组织范围标识决策）。 |
| **Experience Cloud ID服务/ECID** | 跨解决方案使用的永久性访客标识符；通常与标记或Web SDK一起部署。 在旧版Analytics讨论中，仍常用作&#x200B;**Experience Cloud ID**&#x200B;或&#x200B;**MID**。 查看[ID服务概述](https://experienceleague.adobe.com/docs/id-service/using/home.html)。 | 与单个应用程序的旧版Cookie名称或&#x200B;**Experience Platform**&#x200B;标识图概念不同，不过它们可以在实现中关联。 |
| **客户属性** | 您上传和映射的CRM或企业属性，以通过人员服务用于Analytics、Target和相关工作流。 请参阅[客户属性](../services/customer-attributes/attributes.md)主题。 | 如果不检查产品边界，请不要将其与&#x200B;**Audience Manager特征**&#x200B;相等或将其与每个&#x200B;**Real-Time CDP**&#x200B;配置文件字段相等。 |
| **受众库** | CX Enterprise UI ，用于在集成的应用程序间组合和共享受众。 | **Audience Manager**&#x200B;和&#x200B;**Target**&#x200B;也使用“受众”，但分段规则和目标因产品而异。 |
| **区段** (Analytics) | 基于规则的受众定义，您可以在Adobe Analytics中构建受众定义，并在支持时发布到共享受众。 | 在&#x200B;**Audience Manager**&#x200B;中，区段组合了&#x200B;**特征**；命名重叠，但实现不同。 在&#x200B;**Target**&#x200B;中，“受众”在许多地方替换了较早的“区段”标签。 |
| **Assets (Experience Cloud Assets)** | 共享文件夹和文件，用于CX Enterprise营销工作流与已批准的&#x200B;**Creative Cloud**&#x200B;用户之间的协作。 请参阅[Assets概述](../services/assets/experience-cloud-assets.md)。 | 在&#x200B;**Creative Cloud**&#x200B;中，“assets”通常意味着设计文件(PSD、AI、INDD)。 同一个词，不同的分享和治理模式。 |

{style="table-layout:auto"}

