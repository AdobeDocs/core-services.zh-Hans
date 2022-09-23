---
description: 阅读Experience Cloud中的新增功能和更新。
solution: Experience Cloud
title: Experience Cloud 的新增功能
uuid: bc1b1542-1a37-4da1-bcfd-fc86af881642
source-git-commit: eb2ad8a8255915be47b6002a78cc810b522170d2
workflow-type: tm+mt
source-wordcount: '631'
ht-degree: 98%

---


# Experience Cloud 的新增功能

Experience Cloud 中的新增功能和更新概述。

## 2018 年 8 月 {#section_7388CDAB723B49809AABEFEE85CF6378}

修复和改进功能（2018 年 8 月）

* 改进了 Creative Cloud 和 Experience Cloud 之间的资产评论同步。(CORE-15971)
* 添加了用于控制 Experience Cloud 与 Creative Cloud 间资产同步的功能标记。(CORE-15938)
* 改进了受众区段的创建，包括更好的搜索和列表体验。（CORE-5833、CORE-14278）
* 修复了阻止将文件夹从 Experience Cloud 共享到 Creative Cloud 的高优先级问题。(CORE-16677)

## 2018 年 7 月 19 日 {#section_EBB549EBABB7480884A180237ADCCD02}

修复和改进功能（2018 年 7 月）

* 部署了用于控制 Marketing Cloud 到 AEM 和 Marketing Cloud 到 Creative Cloud 之间资产共享的后端功能。(CORE-14386)
* 修复了阻止在某些环境下配置新租户的问题。(CORE-15509)
* 修复了在通过 [!DNL http] 而不是 [!DNL https]（安全）访问 [!DNL experiencecloud.adobe.com] 时将用户重定向到 [!DNL experiencecloud.adobe.com] 的问题。(CORE-15587)
* 修复了阻止对某些新租户显示通知的问题。(CORE-15240)

## 2018 年 6 月 14 日 {#section_7ABC327992CB46B0B8E4A631B8B68899}

修复和改进功能（2018 年 6 月）

* 为管理员启用了指向 GDPR 访问的链接。(CORE-11731)
* 更新了测试版反馈功能，以限制可以附加到反馈的文件类型。(CORE-10474)
* 修复了从 Audience Library 删除受众时出现的问题。(CORE-12792)
* 修复了使用 Federated ID 访问 Workspace 链接时导致屏幕空白的问题。(CORE-11620)

## 2018 年 5 月 10 日 {#section_498AF78DA17C4720AA0F32B51493E550}

[!DNL Adobe Experience Cloud] 界面的新增功能和修复。

| 功能 | 描述 |
|--- |--- |
| 新的管理登录页 | 登录 Experience Cloud 并导航到“管理”页面时，会提供一个新的直观界面，帮助您快速访问 Experience Cloud 应用程序和核心服务。 |

{style=&quot;table-layout:auto&quot;}

**修复**

* 修复了由于 Scene7 更新导致图像上传失败的问题。(CORE-12746)
* 根据 PCI 的要求进行了更新，以放弃对 TLS 1.0 协议的支持，进而消除安全漏洞。(CORE-7695)

## 2017 年 10 月 26 日 {#section_11195859B4094177A939C0561428B525}

**已知问题**

通知电子邮件摘要中缺少有关计划维护/产品更新的许多维护通知。我们努力确保在电子邮件摘要中包含所有维护通知。

## 2017 年 8 月 8 日 {#section_2313A875454044F490B418506DD24593}

| 功能 | 描述 |
|--- |--- |
| 通知 - 粒度设置 | 您可以为产品和应用程序事件及活动启用通知，其中包括有关[客户属性](attributes.md)上传活动的通知。 |
| 通知 - 维护通知 | 在“通知”设置中，您可以为产品和应用程序启用维护通知。 |
| 适用于 Experience Cloud 解决方案的 Admin Console | 新的 Experience Cloud 客户可以开始使用 Admin Console，该控制台是在整个组织中管理 Adobe 权利的中心位置。<br>迁移到管理控制台以进行用户管理的过程将分批进行。Adobe 在需要进行迁移时会联系您（系统管理员）。<br>Analytics 管理员，请参阅 [Analytics 迁移](https://experienceleague.adobe.com/docs/analytics/admin/user-product-management/user-management/migrate-users/c-migration-tool.html?lang=zh-Hans)。 |

{style=&quot;table-layout:auto&quot;}

## 2017 年 5 月 22 日 {#section_242FE649FA1B4BFA88EC6E353D175ACC}

| 功能 | 描述 |
|--- |--- |
| 批量报表包映射 | 在“管理”>“报表包映射”中，现在可以选择多个报表包，然后将它们映射到某个组织。（以前，必须单独映射每个报表包。）<br>[将多个报表包映射到](core-services.md)一个组织有助于在 Experience Cloud 中启用跨应用程序功能和服务。 |
| 针对 Experience Cloud 受众的更新 | **应用报表包**<br>&#x200B;您现在可以将报表包应用于所有[受众规则](t-audience-create.md)。（以前，必须在每个规则定义中指定报表包。）<br>**属性和变量**<br>&#x200B;除 eVar 和事件之外，您现在可以在实时受众中包含 Analytics 属性和默认变量。 |

{style=&quot;table-layout:auto&quot;}

## 2016 年 11 月 8 日 - 16.11.1 {#section_7065A9BCCDF544C2BB37E9A7D661EA6A}

| 功能 | 描述 |
|--- |--- |
| 配置文件和密码更新 | 用户不能再编辑编辑配置文件 > 配置文件和密码中个人详细信息下方的 IMS 用户配置文件信息。用户将会被重定向到 `accounts.adobe.com`。该更新适用于所有身份类型（Adobe ID、Enterprise 和 Federated）。 |

{style=&quot;table-layout:auto&quot;}

**修复**

* 修复了技术密码的问题，该问题导致在 Creative Cloud 和 Experience Cloud 之间共享文件夹时出错。（MAC-31067、MAC-32014）
* 修复了在 10 月份发布后的 Assets 核心服务中发现的某些文件类型（包括 PDF）的上传问题。(MAC-32517)
