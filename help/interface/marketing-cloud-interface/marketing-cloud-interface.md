---
description: Experience Cloud 中的新增功能和更新概述。
keywords: 核心服务
seo-description: Experience Cloud 中的新增功能和更新概述。
seo-title: Experience Cloud 的新增功能
solution: Experience Cloud
title: Experience Cloud 的新增功能
uuid: bc1b 1542-a37-4da1-belamer-fc86 af881642
translation-type: tm+mt
source-git-commit: af5339fe58ce884345804574c209907d6504a483

---


# Experience Cloud 的新增功能

Experience Cloud 中的新增功能和更新概述。

## 2018 年 8 月 {#section_7388CDAB723B49809AABEFEE85CF6378}

修复和改进于2018年月。

* 改进了 Creative Cloud 和 Experience Cloud 间的资产注释同步。(CORE-15971)
* 添加了功能标志以控制Experience Cloud-Creative Cloud资产同步。(CORE-15938)
* 改进了 Audience 区段创建，包括优化的搜索和列表体验。（CORE-5833、CORE-14278）
* 修复了阻止从MAC到Creative Cloud共享文件夹的高优先级问题。(CORE-16677)

## 2018 年 7 月 19 日 {#section_EBB549EBABB7480884A180237ADCCD02}

修复和改进于2018年月。

* 部署了一项后端功能，以控制“Marketing Cloud 到 AEM”与“Marketing Cloud 到 Creative Cloud”之间的资产共享。(CORE-14386)
* 修复了在某些环境中阻止配置新租户的问题。(CORE-15509)
* 修复了在通过 [!DNL http] 而不是 [!DNL https]（安全）访问 [!DNL experiencecloud.adobe.com] 时将用户重定向到 [!DNL marketing.adobe.com] 的问题。(CORE-15587)
* 修复了阻止一些新租户接收通知的问题。(CORE-15240)

## 2018年月14日 {#section_7ABC327992CB46B0B8E4A631B8B68899}

2018 年 6 月的修复和改进功能。

* 为管理员启用了一个指向 GDPR 访问权限的链接。(CORE-11731)
* 更新了测试版反馈功能，以限制可以附加到反馈中的文件类型。(CORE-10474)
* 修复了从 Audience Library 中删除受众的问题。(CORE-12792)
* 修复了使用 Federated ID 访问工作区链接时导致空白屏幕的问题。(CORE-11620)

## 2018 年 5 月 10 日 {#section_498AF78DA17C4720AA0F32B51493E550}

[!DNL Adobe Experience Cloud] 界面的新增功能和修复。

| 功能 | 描述 |
|--- |--- |
| 新管理登陆页面 | 当您登录 Experience Cloud 并导航到“管理”页面时，可以使用新的直观界面来帮助您快速访问 Experience Cloud 解决方案和核心服务。 |
**修复**

* 修复了由于 Scene7 更新导致图像上载失败的问题。(CORE-12746)
* 已根据 PCI 的规定进行更新，取消对 TLS 1.0 协议的支持以消除安全漏洞。(CORE-7695)

## 2017年10月26日 {#section_11195859B4094177A939C0561428B525}

**已知问题**

有关计划维护/产品更新的诸多维护通知在通知电子邮件摘要中缺失。我们正在努力确保使所有维护通知都包含在电子邮件摘要中。

## 2017 年 8 月 8 日 {#section_2313A875454044F490B418506DD24593}

| 功能 | 描述 |
|--- |--- |
| 通知 - 粒度设置 | 您可以启用产品和解决方案事件和活动的通知，包括有关[客户属性](../attributes/attributes.md)上传活动的通知。 |
| 通知 - 维护通知 | 在“通知”设置中，您可以启用产品和解决方案的维护通知。 |
| Experience Cloud 解决方案的管理控制台 | 新的 Experience Cloud 客户可以开始使用管理控制台，它是一个用于在您的整个组织内管理 Adobe 权限的中心位置。<br>迁移到管理控制台以进行用户管理的过程将分批进行。Adobe 将在需要进行迁移时通知您（系统管理员）。<br>对于 Analytics 管理员，请参阅 [Analytics 迁移](https://marketing.adobe.com/resources/help/en_US/experience-cloud/admin-console/analytics-migration/)。 |

## 2017年月22日 {#section_242FE649FA1B4BFA88EC6E353D175ACC}

| 功能 | 描述 |
|--- |--- |
| 批量报表包映射 | 在管理 &gt; 报表包映射中，现在可以选择多个报表包，然后将它们映射到某个组织。（以前，必须单独映射每个报表包。）<br>[将多个报表包映射到一个组织有助于在 Experience Cloud 中启用跨解决方案功能和服务。](../core-services/core-services.md) |
| 针对 Experience Cloud 受众的更新 | **应用报告套件您**<br>现在可以将报表包应用于 [所有受众规则](../audience-library/t-audience-create.md)。（以前，必须在每个规则定义中指定报表包。）<br>**Props和变量您**<br>现在可以在实时受众中包括Analytics prop和默认变量(除eVar和事件之外)。 |

## 2016年11月日-16.11.1 {#section_7065A9BCCDF544C2BB37E9A7D661EA6A}

| 功能 | 描述 |
|--- |--- |
| “配置文件和密码”更新 | 用户不能再编辑编辑配置文件 &gt; 配置文件和密码中个人详细信息下方的 IMS 用户配置文件信息。用户将会被重定向到 `accounts.adobe.com`。这种情况适用于所有身份类型（Adobe ID、Enterprise ID 和 Federated ID）。 |

**修复**

* 修复了导致在 Creative Cloud 和 Experience Cloud 之间共享文件夹时出错的技术密码问题。（MAC-31067、MAC-32014）
* 修复了上传某些类型的文件（包括 PDF）时出现的问题，此问题发生在 10 月发行版之后的 Assets 核心服务中。(MAC-32517)
