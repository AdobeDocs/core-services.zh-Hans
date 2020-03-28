---
description: Experience Cloud 中的新增功能和更新概述。
keywords: core services
seo-description: Experience Cloud 中的新增功能和更新概述。
seo-title: Experience Cloud 的新增功能
solution: Experience Cloud
title: Experience Cloud 的新增功能
uuid: bc1b1542-1a37-4da1-bcfd-fc86af881642
translation-type: tm+mt
source-git-commit: 43de353155c640b3ddc519147c94d7e9ffcafe4e

---


# Experience Cloud 的新增功能

Experience Cloud 中的新增功能和更新概述。

## 2018 年 8 月 {#section_7388CDAB723B49809AABEFEE85CF6378}

2018 年 8 月的修复和改进功能。

* 改进了跨Creative Cloud和Experience Cloud同步资产注释的功能。 (CORE-15971)
* 添加了用于控制 Experience Cloud 与 Creative Cloud 间资产同步的功能标记。(CORE-15938)
* 改进了受众区段的创建，包括更好的搜索和列表体验。 (CORE-5833, CORE-14278)
* 修复了阻止将文件夹从 MAC 共享到 Creative Cloud 的高优先级问题。(CORE-16677)

## 2018 年 7 月 19 日 {#section_EBB549EBABB7480884A180237ADCCD02}

2018 年 7 月的修复和改进功能。

* 部署了后端功能，以控制Marketing Cloud到AEM和Marketing Cloud到Creative Cloud之间的资产共享。 (CORE-14386)
* 修复了阻止在某些环境上提供新租户的问题。 (CORE-15509)
* 修复了在通过 [!DNL http] 而不是 [!DNL https]（安全）访问 [!DNL experiencecloud.adobe.com] 时将用户重定向到 [!DNL experiencecloud.adobe.com] 的问题。(CORE-15587)
* 修复了阻止某些新租户通知的问题。 (CORE-15240)

## 2018 年 6 月 14 日 {#section_7ABC327992CB46B0B8E4A631B8B68899}

2018年6月的修复和改进。

* 已为管理员启用指向GDPR访问的链接。 (CORE-11731)
* 更新的测试版反馈功能可限制可附加到反馈的文件类型。 (CORE-10474)
* 修复了从受众库中删除受众的问题。 (CORE-12792)
* 修复了使用Federated ID访问Workspace链接时导致空白屏幕的问题。 (CORE-11620)

## 2018 年 5 月 10 日 {#section_498AF78DA17C4720AA0F32B51493E550}

[!DNL Adobe Experience Cloud] 界面的新增功能和修复。

| 功能 | 描述 |
|--- |--- |
| 新的管理登陆页 | 登录到Experience Cloud并导航到“管理”页面时，会提供一个新的直观界面，帮助您快速访问Experience Cloud解决方案和核心服务。 |

**修复**

* 修复了由于Scene7更新而导致图像上传失败的问题。 (CORE-12746)
* 根据PCI的要求，更新以停止对TLS 1.0协议的支持，以消除安全漏洞。 (CORE-7695)

## 2017 年 10 月 26 日 {#section_11195859B4094177A939C0561428B525}

**已知问题**

通知电子邮件摘要中缺少许多与计划维护／产品更新相关的维护通知。 我们正在努力确保所有维护通知都包含在电子邮件摘要中。

## August 8, 2017 {#section_2313A875454044F490B418506DD24593}

| 功能 | 描述 |
|--- |--- |
| 通知——粒度设置 | 您可以启用产品和解决方案事件和活动的通知，包括有关[客户属性](../attributes/attributes.md)上传活动的通知。 |
| 通知——维护通知 | 在“通知”设置中，您可以为产品和解决方案启用维护通知。 |
| 适用于Experience Cloud解决方案的Admin Console | 新的Experience Cloud客户可以开始使用Admin Console，它是管理整个组织中Adobe授权的中心位置。<br>迁移到管理控制台以进行用户管理的过程将分批进行。Adobe 将在需要进行迁移时通知您（系统管理员）。<br>分析管理员，请参阅 [分析迁移](https://docs.adobe.com/content/help/en/analytics/admin/user-product-management/user-management/migrate-users/c-migration-tool.html)。 |

## 2017 年 5 月 22 日 {#section_242FE649FA1B4BFA88EC6E353D175ACC}

| 功能 | 描述 |
|--- |--- |
| 批量报表包映射 | 在管理 > 报表包映射中，现在可以选择多个报表包，然后将它们映射到某个组织。（以前，必须单独映射每个报表包。）<br>[将多个报表包映射到一个组织有助于在 Experience Cloud 中启用跨解决方案功能和服务。](../core-services/core-services.md) |
| 针对 Experience Cloud 受众的更新 | **应用报表包&#x200B;**<br>您现在可以将报表包应用于所有[受众规则](../audience-library/t-audience-create.md)。（以前，必须在每个规则定义中指定报表包。）<br>**属性和变量**<br>除 eVar 和事件之外，您现在可以在实时受众中包含 Analytics 属性和默认变量。 |

## 2016 年 11 月 8 日 - 16.11.1 版{#section_7065A9BCCDF544C2BB37E9A7D661EA6A}

| 功能 | 描述 |
|--- |--- |
| 更新到用户档案和密码 | 用户不能再编辑编辑配置文件 > 配置文件和密码中个人详细信息下方的 IMS 用户配置文件信息。用户将会被重定向到 `accounts.adobe.com`。这种情况适用于所有身份类型（Adobe ID、Enterprise ID 和 Federated ID）。 |

**修复**

* 修复了在Creative Cloud和Experience Cloud之间共享文件夹时出现错误的技术密码问题。 (MAC-31067、MAC-32014)
* 修复了在10月版本发布后在资产核心服务中发现的某些文件类型（包括PDF）的上传问题。 (MAC-32517)
