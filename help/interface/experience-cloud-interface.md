---
description: '了解如何在Experience Cloud中登录和关于中央界面组件。 了解全局搜索、您的帐户首选项以及如何导航界面和获取帮助。 '
solution: Experience Cloud
title: 'Experience Cloud 中央 UI 组件 '
feature: “中央界面组件”
topic: 管理
role: Admin, User
level: Beginner, Intermediate, Experienced
source-git-commit: c9a6059b0af9c6229fd72580f997c1c6f2dfbbe4
workflow-type: tm+mt
source-wordcount: '718'
ht-degree: 50%

---

# Experience Cloud 界面帮助

Experience Cloud 的中央界面组件包括的功能使您能够：

* 登录并访问您的应用程序和服务
* 使用全局搜索查找产品帮助和业务对象
* 管理您的帐户首选项（警报、通知和订阅）

## 浏览器支持Experience Cloud {#browser}

为获得最佳性能，已针对最常用的浏览器（包括最新版本）以及之前的两个版本对Experience Cloud进行优化。

* Chrome
* Edge
* Firefox
* Opera
* Safari

如果您的浏览器未列出，则仍可能支持它，但建议您使用列出的浏览器之一。

>[!NOTE]
>
>并非所有在Experience Cloud域上运行的应用程序都支持所有浏览器。 如果您不确定，请查看特定应用程序的文档。

## Experience Cloud中的语言支持 {#languages}

Experience Cloud支持在Adobe用户帐户首选项中设置的每个用户首选语言。 目前支持的语言包括：

* 中文
* 英语
* 法语
* 德语
* 意大利语
* 日语
* 朝鲜语
* 葡萄牙语
* 西班牙语
* 台湾语

尽管所有应用程序团队都致力于提供全球语言支持，但并非所有应用程序都以上述所有语言提供。 如果Experience Cloud应用程序不支持主语言，您还可以将辅助语言设置为默认（如果适用）。 可以在[Experience Cloud用户首选项](https://experience.adobe.com/preferences)中执行此操作。

## 登录到 Experience Cloud {#signin}

登录并验证您是否处于正确的[组织](organizations.md)中。

1. 导航到 [Adobe Experience Cloud](https://experience.adobe.com)。
1. 选择&#x200B;**[!UICONTROL 使用Adobe ID]**&#x200B;登录。
1. 确认您处于正确的组织中。

   ![](assets/organizations-menu.png)

   要验证您是否已登录到正确的[organization](organizations.md)，请单击您的个人资料头像以查看组织名称。 如果您有权访问多个组织，则还可以在标题栏中查看并切换到另一个组织。

   如果贵组织使用Federated ID，则Experience Cloud允许您使用贵组织的单点登录进行登录，而无需输入您的电子邮件地址和密码。 为此，请将`#/sso:@domain`添加到Experience CloudURL(`https://experience.adobe.com`)。

   例如，对于具有Federated ID和域`adobecustomer.com`的组织，请将您的URL链接设置为`https://experience.adobe.com/#/sso:@adobecustomer.com`。 您还可以通过将此URL添加书签并附加应用程序路径，直接转到特定应用程序。 (例如，对于Adobe Analytics,`https://experience.adobe.com/#/sso:@adobecustomer.com/analytics`。)

## 访问 Experience Cloud 应用程序 {#navigation}

登录到 Experience Cloud 后，您可以从统一页头中快速访问您的所有应用程序、服务和组织。

选择应用程序选择器![](assets/menu-icon.png)以访问您拥有的Experience Cloud服务。

![](assets/platform-core-services.png)

## Experience Cloud 中的搜索和支持 {#search}

利用 Experience Cloud 搜索功能，您可以搜索关于 [Experience League](https://experienceleague.adobe.com/?lang=zh-Hans#home) 的帮助（文档、教程和课程）。

![](assets/search-menu.png)

通过[!UICONTROL 帮助]菜单，您还可以访问：

* **[!UICONTROL 支持]：**&#x200B;创建支持工单或使用 Twitter 联系支持[!UICONTROL 支持]部门。
* **[!UICONTROL 反馈]：**&#x200B;使用反馈联系 Adobe，告诉我们您的想法。
* **[!UICONTROL 状态]：**&#x200B;导航到 `https://status.adobe.com/experience_cloud`，检查产品操作状态并[!UICONTROL 管理订阅]。
* **[!UICONTROL 开发人员连接]：**&#x200B;导航到 `adobe.io` 并查找开发人员文档。

## 帐户首选项 {#account-menu}

在帐户首选项菜单中，您可以：

* 指定深色主题（并非所有应用程序都支持此主题）
* 搜索[组织](organizations.md)
* 注销
* 配置帐户[首选项、通知和订阅](#preferences)

### 管理 Experience Cloud [!UICONTROL 首选项] {#preferences}

Experience Cloud 首选项包括通知、订阅和警报。

从帐户菜单![](assets/preferences-icon-sm.png)中选择&#x200B;**[!UICONTROL 首选项]**&#x200B;以管理首选项。

![](assets/preferences-page.png)

在 [!UICONTROL Experience Cloud 首选项]上，您可以配置以下功能：

| 功能 | 描述 |
|--- |--- |
| 默认[组织](organizations.md) | 选择您要在启动 Experience Cloud 时看到的组织。 |
| [!UICONTROL 订阅] | 选择您要订阅的产品和类别。[!UICONTROL 通知]弹出窗口和电子邮件中的通知。 |
| [!UICONTROL 优先级] | 选择您希望视为高优先级的类别。这些类别标有“高”标签，可以配置为像警报一样发送。 |
| [!UICONTROL 警报] | 选择您希望在浏览器中显示警报所针对的通知。警报会在窗口右上角出现几秒钟。 |
| 电子邮件 | 指定您希望接收通知电子邮件的频率。（不发送、即时、每日或每周。） |

{style=&quot;table-layout:auto&quot;}

## 通知和公告 {#notifications}

选择&#x200B;**[!UICONTROL 通知]**&#x200B;以查看对您重要的通知和Adobe中的公告。

![](assets/notifications-menu-small.png)

您可以在 [Experience Cloud 首选项](#preferences)中配置通知。
