---
description: 了解 Experience Cloud 的中央界面组件。在 Admin Console 中获取用户和产品管理帮助，启用 Experience Cloud Service 的应用程序。获取受众库、客户属性、Experience Cloud Assets 等方面的帮助。
title: Experience Cloud 界面文档
uuid: aec6f689-e617-4876-ae6c-e961cfcb991a
feature: Central Interface Components
topic: Administration
role: Admin
level: Experienced
exl-id: aedad5cb-3282-4a97-8e7e-6d65f7b75ba9
source-git-commit: 5df8104d3d148cc7bda823b27bf96429ddb6018d
workflow-type: tm+mt
source-wordcount: '790'
ht-degree: 80%

---

# Experience Cloud 中央界面概述组件

[Experience Cloud](https://experience.adobe.com) 是 Adobe 综合系列的数字营销应用程序、产品和服务。通过其直观界面，您可以快速访问云应用程序、产品功能和服务。

![Experience Cloud](assets/landing.png)

通过 Experience Cloud 的标题，您可以：

* 访问您的所有Experience Cloud应用程序和服务
* 从“帮助”菜单中，搜索产品文档、教程和社区帖子。在 Experience League 中查看结果。
* 使用全局搜索在“搜索”字段中全局搜索业务对象（仅限 Experience Platform 用户）。
* 管理您的帐户[首选项](features/account-preferences.md)（警报、通知和订阅）

## 登录到 Experience Cloud {#signin}

登录并验证您是否处于正确的[组织](administration/organizations.md)中。

1. 导航到 [Adobe Experience Cloud](https://experience.adobe.com)。
1. 请输入您的 Adobe 电子邮件地址，然后选择&#x200B;**[!UICONTROL 继续]**。
1. 选择帐户。
1. 键入您的密码。
1. 验证您是否处于正确的组织中。

   ![验证您是否处于正确的组织中](assets/organizations-menu.png)

   **验证您的组织**

   [组织](administration/organizations.md)显示在接口标头中。

   如果您的组织使用 Federated ID，则 Experience Cloud 允许您使用组织的单点登录进行登录，而无需输入您的电子邮件地址和密码。将 `#/sso:@domain` 添加到 Experience Cloud URL (`https://experience.adobe.com`) 以完成此任务。

   例如，对于带 Federated ID 和域 `adobecustomer.com` 的组织，请将 URL 链接设置为 `https://experience.adobe.com/#/sso:@adobecustomer.com`。您还可以通过为此 URL 添加书签并追加应用程序路径，直接转到特定应用程序。（例如，对于 Adobe Analytics，使用 `https://experience.adobe.com/#/sso:@adobecustomer.com/analytics`。）

## 访问 Experience Cloud 应用程序 {#navigation}

登录到 Experience Cloud 后，您可以从统一页头中快速访问您的所有应用程序、服务和组织。

要访问组织中为您预配的 Experience Cloud 应用程序和服务，请转到应用程序选择器 ![菜单](assets/menu-icon.png)。

![访问 Experience Cloud 应用程序](assets/platform-core-services.png)

## 获取帮助和支持 {#support}

使用标头中的&#x200B;**[!UICONTROL 帮助中心]** （![资源](assets/help-icon.png)）访问学习和帮助，包括有关[Experience League](https://experienceleague.adobe.com/?lang=zh-Hans#home)的帮助内容（文档、教程和课程）以及各个应用程序的其他资源。 您也可以提交开放式的反馈并创建优先支持服务单。

![获取帮助和支持](assets/search-menu.png)

通过[!UICONTROL 帮助]菜单，您还可以访问：

* **[!UICONTROL 支持]：**&#x200B;创建支持工单或使用 Twitter 联系支持[!UICONTROL 支持]部门。
* **[!UICONTROL 反馈]：**&#x200B;共享您对 Experience Cloud 体验的反馈。您的反馈将用于改进 Adobe 的支持和服务。
* **[!UICONTROL 状态]：**&#x200B;导航到 `https://status.adobe.com/experience_cloud`，检查产品操作状态并[!UICONTROL 管理订阅]。
* **[!UICONTROL 开发人员连接]：**&#x200B;导航到 `adobe.io` 并查找开发人员文档。

## 管理您的用户配置文件

在[!UICONTROL 配置文件]菜单中，您可以：

* 指定深色主题（并非所有应用程序都支持此主题）
* 管理 Experience Cloud [首选项](features/account-preferences.md)
* 选择或搜索[组织](administration/organizations.md)
* 查看[!UICONTROL 法律声明]
* 注销
* 配置帐户首选项、通知和订阅

## 查看产品内通知和公告 {#notifications}

单击铃铛图标查看通知和公告。 公告可以是相关且切实可行的更新，包括产品版本、维护通知、共享项和批准申请。

![通知和公告](assets/notifications-menu-small.png)

若要管理通知和警报，请参阅[帐户首选项和通知](features/account-preferences.md)


## 新增功能

了解对Experience Cloud中央界面组件的最新增强功能。

>[!BEGINTABS]

>[!TAB Slack与Experience Cloud]的集成

您可以配置帐户首选项以将Experience Cloud通知发送到[!DNL Slack]频道。

[!BADGE Beta]{type=Informative url="https://experienceleague.adobe.com/en/docs/core-services/interface/features/account-preferences#notifications" tooltip="了解Slack"}


>[!TAB 全新 Campaign Web 用户界面]

体验全新 Adobe Campaign 用户界面。更加现代化、直观和充满活力！

[![图像](assets/do-not-localize/learn-more-button.svg)](start/campaign-ui.md#ac-web-ui)


>[!TAB 即将对推送渠道做出的更改]

Android Firebase Cloud Messaging (FCM) 服务的一些重要更改将于 2024 年发布，并将影响您的 Adobe Campaign 实施。您可能需要更新 Android 推送消息的订阅服务配置，才能支持此更改。您已经可以检查并执行操作。

[![图像](assets/do-not-localize/learn-more-button.svg)](../technotes/upgrades/push-technote.md)



>[!ENDTABS]

## 从基础知识开始

<table style="table-layout:fixed">
  <tr style="border: 0;">
    <td>
    <a href="start/whats-new.md"><img src="assets/do-not-localize/start-capabilities.png"></a>
    <div><strong>主要功能</strong><br/>探索 Adobe Campaign v8 的跨渠道营销活动管理的主要功能。</div>
    </td>
    <td>
    <a href="start/connect.md"><img src="assets/do-not-localize/start-connect.jpeg"></a>
    <div><strong>连接到 Campaign v8</strong><br/>了解如何通过安装和配置客户端控制台来连接到 Adobe Campaign v8，并启动营销活动管理之旅。</div><br/>
    </td>
    <td>
    <a href="start/create-message.md"><img src="assets/do-not-localize/start-send.jpeg"></a>
    <div><strong>发送消息</strong><br/>了解如何通过电子邮件、短信、推送通知等各种渠道发送消息。
    </div></td>
    <td>
    <a href="audiences/create-profiles.md"><img src="assets/do-not-localize/start-profiles.png"></a>
    <div><strong>导入用户档案</strong><br/>探索如何在 Adobe Campaign v8 数据库中轻松创建用户档案。手动或通过导入添加用户档案，轻松优化客户数据和自定义营销活动。</div>
    </td>
  </tr>
  <tr style="border: 0;">
    <td align="center"><a href="start/whats-new.md"><img src="assets/do-not-localize/learn-more-button.svg"></a></td>
    <td align="center"><a href="start/connect.md"><img src="assets/do-not-localize/learn-more-button.svg"></a></td>
    <td align="center"><a href="start/create-message.md"><img src="assets/do-not-localize/learn-more-button.svg"></a></td>
    <td align="center"><a href="audiences/create-profiles.md"><img src="assets/do-not-localize/learn-more-button.svg"></a></td>
    </tr>
</table>

## 浏览文档

<table style="table-layout:auto">
  <tr style="border: 0;">
    <td>
      <img src="assets/do-not-localize/icon-start.svg" width="35px">
    <br/>
      <strong>入门</strong><br/><a href="start/campaign-ui.md">用户界面</a> - <a href="start/ac-components.md">组件和流程</a> - <a href="start/v7-to-v8.md">从 Classic v7 到 v8</a> - <a href="start/campaign-faq.md">常见问题</a>
    </td>
    <td>
      <img src="assets/do-not-localize/icon-experience.svg" width="35px">
    <br/>
      <strong>客户体验</strong><br/><a href="../automation/workflow/about-workflows.md" target="_blank">使用工作流实现自动化</a> - <a href="../automation/campaigns/set-up-campaigns.md" target="_blank">活动编排</a> - <a href="interaction/interaction.md">决策管理</a> - <a href="send/personalize.md">个性化</a>
    </td>
    <td>
      <img src="assets/do-not-localize/icon-send.svg" width="35px">
    <br/>
      <strong>发送消息</strong><br/><a href="start/create-message.md">入门</a> - <a href="send/preview-and-proof.md">预览和验证</a> - <a href="send/predictive.md">发送时间优化</a> - <a href="reporting/gs-reporting.md">报告与分析</a>
    </td>
  </tr>
  <tr style="border: 0;">
    <td>
      <img src="assets/do-not-localize/icon_profile-audience.svg" width="35px">
    <br/>
      <strong>用户档案和受众</strong><br/><a href="audiences/create-profiles.md">添加用户档案</a> - <a href="audiences/create-audiences.md">创建受众</a> - <a href="start/subscriptions.md">管理订阅</a> - <a href="start/privacy.md">隐私</a>
    </td>
    <td>
      <img src="assets/do-not-localize/icon-configure.svg" width="35px">
    <br/>
      <strong>架构与配置</strong><br/><a href="architecture/architecture.md">架构</a> - <a href="start/implement.md">Campaign v8 实施</a> - <a href="connect/integration.md">与其他解决方案连接</a> - <a href="start/gs-permissions.md">用户和权限</a>
    </td>
    <td>
      <img src="assets/do-not-localize/icon-dev.svg" width="35px">
    <br/>
      <strong>开发人员资源</strong><br/><a href="dev/datamodel.md">Campaign v8数据模型</a> - <a href="dev/schemas.md">架构</a> - <a href="dev/api.md">API</a>
    </td>
  </tr>
</table>

## 其他资源

[Adobe Campaign v8 产品说明](https://helpx.adobe.com/cn/legal/product-descriptions/adobe-campaign-managed-cloud-services.html){target="_blank"} - [Adobe Campaign Web 用户界面文档](https://experienceleague.adobe.com/docs/campaign-web/v8/campaign-web-home.html?lang=zh-Hans){target="_blank"} - [教程](https://experienceleague.adobe.com/docs/campaign-learn/tutorials/overview.html?lang=zh-CN){target="_blank"} - [[!DNL Adobe Campaign] 自动化指南](https://experienceleague.adobe.com/docs/campaign/automation/home.html?lang=zh-Hans){target="_blank"} - [Campaign v8 的控制面板](https://experienceleague.adobe.com/docs/control-panel/using/discover-control-panel/key-features.html?lang=zh-Hans){target="_blank"}
