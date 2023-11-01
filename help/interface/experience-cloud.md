---
description: 了解 Experience Cloud 的中央界面组件。该帮助包括如何在 Admin Console 中管理用户和产品、如何启用面向 Experience Cloud 服务的应用程序，并且提供有关受众库、客户属性和 Experience Cloud Assets 等更多方面的帮助。
title: Experience Cloud 界面帮助和文档
uuid: aec6f689-e617-4876-ae6c-e961cfcb991a
feature: Central Interface Components
topic: Administration
role: Admin
level: Experienced
exl-id: aedad5cb-3282-4a97-8e7e-6d65f7b75ba9
source-git-commit: acdf73ddc3bacbf18c069b7fd6afd935a17003a4
workflow-type: tm+mt
source-wordcount: '1347'
ht-degree: 100%

---

# Experience Cloud 中央界面组件指南

[Experience Cloud](https://experience.adobe.com) 是 Adobe 综合系列的数字营销应用程序、产品和服务。通过其直观界面，您可以快速访问云应用程序、产品功能和服务。

![Experience Cloud](assets/landing.png)

通过 Experience Cloud 的标题，您可以：

* 访问您的应用程序和服务
* 从“帮助”菜单中，搜索产品文档、教程和社区帖子。在 Experience League 中查看结果。
* 使用全局搜索在“搜索”字段中全局搜索业务对象（仅限 Experience Platform 用户）。
* 管理您的帐户首选项（警报、通知和订阅）

## 登录到 Experience Cloud {#signin}

登录并验证您是否处于正确的[组织](organizations.md)中。

1. 导航到 [Adobe Experience Cloud](https://experience.adobe.com)。
1. 请输入您的 Adobe 电子邮件地址，然后选择&#x200B;**[!UICONTROL 继续]**。

   管理员可查看 [Experience Cloud 用户身份验证](admin-getting-started.md#migration)，获取身份类型的重要更新 (Business ID)。

1. 选择帐户。
1. 键入您的密码。
1. 验证您是否处于正确的组织中。

   ![验证您是否处于正确的组织中](assets/organizations-menu.png)

   **验证您的组织**

   要验证您是否已登录到正确的[组织](organizations.md)，请单击您的个人资料头像查看组织名称。 如果您有权访问多个组织，也可以直接在标题栏中查看和切换到另一个组织。

   如果您的组织使用 Federated ID，则 Experience Cloud 允许您使用组织的单点登录进行登录，而无需输入您的电子邮件地址和密码。将 `#/sso:@domain` 添加到 Experience Cloud URL (`https://experience.adobe.com`) 以完成此任务。

   例如，对于带 Federated ID 和域 `adobecustomer.com` 的组织，请将 URL 链接设置为 `https://experience.adobe.com/#/sso:@adobecustomer.com`。您还可以通过为此 URL 添加书签并追加应用程序路径，直接转到特定应用程序。（例如，对于 Adobe Analytics，使用 `https://experience.adobe.com/#/sso:@adobecustomer.com/analytics`。）

## 访问 Experience Cloud 应用程序 {#navigation}

登录到 Experience Cloud 后，您可以从统一页头中快速访问您的所有应用程序、服务和组织。

要访问组织中为您预配的 Experience Cloud 应用程序和服务，请转到应用程序选择器 ![菜单](assets/menu-icon.png)。

![访问 Experience Cloud 应用程序](assets/platform-core-services.png)

## Experience Cloud 中的浏览器支持 {#browser}

为了实现最佳性能，Experience Cloud 针对最受欢迎的浏览器（包括最新版本以及上两个版本）进行了优化。

* Chrome
* Edge
* Firefox
* Opera
* Safari

如果您的浏览器非上述浏览器，则可能仍受支持，但建议您使用列出的浏览器之一。

>[!NOTE]
>
>并非所有在 Experience Cloud 域上运行的应用程序都支持所有浏览器。如果您不确定，请查看特定应用程序的文档。

## Experience Cloud 中的语言支持 {#languages}

Experience Cloud 支持每个用户的首选语言，如您的 Adobe 用户帐户偏好设置中所设定。当前支持的语言为：

* 简体中文
* 英语
* 法语
* 德语
* 意大利语
* 日语
* 朝鲜语
* 葡萄牙语
* 西班牙语
* 繁体中文

虽然所有应用程序团队都致力于提供全球语言支持，但并非所有应用程序都具有上述所有语言版本。如果 Experience Cloud 应用程序不支持您的主要语言，您也可以将辅助语言设置为默认语言（如果适用）。可以在 [Experience Cloud 用户偏好设置](https://experience.adobe.com/preferences)中执行此操作。

## 获取帮助和支持 {#support}

使用标头中的帮助图标（![资产](assets/help-icon.png)）访问学习和帮助内容，包括有关 [Experience League](https://experienceleague.adobe.com/?lang=zh-Hans#home) 的帮助内容（文档、教程和课程）以及各个应用程序的其他资源。您也可以提交开放式的反馈并创建优先支持服务单。

![获取帮助和支持](assets/search-menu.png)

通过[!UICONTROL 帮助]菜单，您还可以访问：

* **[!UICONTROL 支持]：**&#x200B;创建支持工单或使用 Twitter 联系支持[!UICONTROL 支持]部门。
* **[!UICONTROL 反馈]：**&#x200B;共享您对 Experience Cloud 体验的反馈。您的反馈将用于改进 Adobe 的支持和服务。
* **[!UICONTROL 状态]：**&#x200B;导航到 `https://status.adobe.com/experience_cloud`，检查产品操作状态并[!UICONTROL 管理订阅]。
* **[!UICONTROL 开发人员连接]：**&#x200B;导航到 `adobe.io` 并查找开发人员文档。

## 用户个人资料和帐户偏好设置 {#preferences}

Experience Cloud 首选项包括通知、订阅和警报。在帐户首选项菜单中，您可以：

* 指定深色主题（并非所有应用程序都支持此主题）
* 搜索[组织](organizations.md)
* 注销
* 配置帐户首选项、通知和订阅

要管理首选项，请从帐户菜单 ![首选项](assets/preferences-icon-sm.png) 中选择&#x200B;**[!UICONTROL 首选项]**。

![用户个人资料和帐户偏好设置](assets/preferences-page.png)

在 [!UICONTROL Experience Cloud 首选项]上，您可以配置以下功能：

| 功能 | 描述 |
|--- |--- |
| 默认[组织](organizations.md) | 选择您要在启动 Experience Cloud 时看到的组织。 |
| [!UICONTROL 产品数据收集] | 选择 Adobe 可以使用哪些技术来收集有关您如何使用 Adobe 产品的数据。 |
| [!UICONTROL 个性化的学习推荐和促销] | 选择您希望通过何种方式获得有关 Adobe 产品的个性化帮助。此帮助可通过电子邮件、产品中消息以及 Experience League 社区提供。[了解详情。](personalized-learning-preferences.md) |
| [!UICONTROL 订阅] | 选择您要订阅的产品和类别。[!UICONTROL 通知]弹出窗口和电子邮件中的通知。 |
| [!UICONTROL 优先级] | 选择您希望视为高优先级的类别。这些类别标有“高”标签，可以配置为像警报一样发送。 |
| [!UICONTROL 警报] | 选择您希望在浏览器中显示警报的通知。警报会在窗口右上角出现几秒钟。 |
| 电子邮件 | 指定您希望接收通知电子邮件的频率。（不发送、即时、每日或每周。） |

{style="table-layout:auto"}

## 通知和公告 {#notifications}

选择&#x200B;**[!UICONTROL 通知]**，即可收到相关可操作更新的通知，包括产品版本、维护通知、共享项和批准申请。

![通知和公告](assets/notifications-menu-small.png)

## Experience Cloud 域 {#domains}

Experience Cloud 使用以下主机来交付应用程序、提高性能和改善产品体验。Adobe 建议将这些域添加到防火墙的允许列表以获得最佳体验。其他域也可用于特定的 Experience Cloud 应用程序，例如 Adobe Analytics。有关更多信息，请查看这些应用程序的文档。

| 技术 | 域 |
|--- |--- |
| Adobe Experience Cloud 域 | `adobe.com`、`adobe.net`、`adobe.io` |
| Adobe Identity Management Service (IMS) | `adobelogin.com` |
| Experience Cloud 字体 | `typekit.net` |
| Adobe 数据收集（用于产品指导和帮助） | `adobedtm.com` |
| Gainsight（用于产品指导和帮助） | `esp.aptrinsic.com` |

## 获取有关管理和跨应用程序服务的帮助

本指南提供的帮助内容涉及如何在 Admin Console 中管理 Experience Cloud 用户和产品，以及如何启用面向平台服务的应用程序。另外，您还可以获取有关受众库、客户属性、Experience Cloud Assets 等更多方面的帮助：

* [[!UICONTROL 受众库]](audience-library.md)
* [[!UICONTROL 客户属性]](attributes.md)
* [[!UICONTROL 触发器]](triggers.md)
* [Experience Cloud [!UICONTROL Assets]](experience-cloud-assets.md)
* [Experience Cloud Cookie](cookies-privacy.md)
* [用户和产品管理](admin-getting-started.md) (Admin Console)
* [为核心服务启用应用程序](core-services.md)
* [常见问题解答](admin-getting-started.md)
* [组织和帐户关联](organizations.md)
* [集成](marketing-cloud-integrations.md)
* [将 Adobe Target 与 Experience Cloud 集成](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html?lang=zh-Hans)
* [Experience Cloud 隐私和安全性概述](assets/Adobe-Marketing-Cloud-Privacy-and-Security-Overview.pdf)
* [DNS 预获取](admin-getting-started.md#concept_6BC8C6856E3644F8956D7AD0A96383B7)

## 指南

相关的 Experience Cloud 指南包括：

* [Adobe Mobile](https://experienceleague.adobe.com/docs/mobile-services/using/home.html?lang=zh-Hans)
* [Experience Platform Co-op Graph](https://experienceleague.adobe.com/docs/device-co-op/using/home.html?lang=zh-Hans)
* [Exchange](https://exchange.adobe.com/experiencecloud)
* [Experience Cloud ID 服务](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=zh-Hans)
* [Experience Platform 数据收集/Launch](https://experienceleague.adobe.com/docs/launch.html?lang=zh-Hans)
* [Experience Cloud Debugger](https://experienceleague.adobe.com/docs/debugger/using/experience-cloud-debugger.html?lang=zh-Hans)
* [[!UICONTROL Dynamic Tag Management]](https://experienceleague.adobe.com/docs/experience-platform/tags/home.html?lang=zh-Hans)

## 教程

充分利用以下 Experience League 中的自助式教程和简短的使用说明：

* [Experience League 中的所有教程](https://experienceleague.adobe.com/?lang=en#quick-how-tos)
* [Experience Platform 教程](https://experienceleague.adobe.com/docs/platform-learn/data-collection/overview.html?lang=zh-Hans)
* [实时客户数据平台](https://experienceleague.adobe.com/docs/platform-learn/tutorials/application-services/rtcdp/understanding-the-real-time-customer-data-platform.html?lang=zh-Hans)

## 发行说明和相关的 Experience Cloud 帮助

* [所有 Experience Cloud 应用程序的产品文档](https://experienceleague.adobe.com/docs/home.html?lang=zh-Hans) – 浏览 Experience Cloud 学习和支持页面以获取帮助
* [发行说明和产品更新](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html?lang=zh-Hans) – Experience Cloud 的新增功能，订阅可获取更新
* [实施核心服务的教程](https://experienceleague.adobe.com/docs/platform-learn/data-collection/overview.html?lang=zh-Hans) – 浏览有关核心服务的视频和教程
* [Experience League 的专家帮助](https://experienceleague.adobe.com/cn) – 从专家和社区获得指导性学习
* [教育和培训](https://helpx.adobe.com/cn/learning.html?promoid=KAUDK) – 与 Adobe 互动以确保您能够充分利用 Adobe 的产品
* [客户体验博客](https://blog.adobe.com/en/topics/digital-transformation) – 阅读 Experience Cloud 博客
* [客户关怀](https://experienceleague.adobe.com/?support-solution=General#support) – 联系 Adobe 客户关怀部门
