---
description: 优惠管理、如何访问以及如何授予用户权限的概述。
seo-description: 优惠管理、如何访问以及如何授予用户权限的概述。
seo-title: 入门指南
title: 入门指南
uuid: 28d83606-ee36-4bbf-b52d-bbe8b097f6d5
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 43de353155c640b3ddc519147c94d7e9ffcafe4e

---


# Adobe优惠管理 {#section_07CBD4C01F4049A5A19781737D2DCD35}

[!UICONTROL 优惠管理] ，可在Experience Cloud的所有渠道中创建、管理和决策优惠。 它用作一个中心优惠目录，您可以将合格规则和多段内容与每个优惠对象关 _联。_ 您可以跨渠道和位置发布这些优惠，并在每次互动中为每位客户提供最佳优惠。 这些功能使您能够以跨客户体验一致和协调的方式持续为客户提供最佳优惠。

优势包括：

* 通过在电子邮件中提供更个性化的优惠，改进了电子邮件活动性能。
* 改进的工作流程：营销团队可以通过创建单个投放来改进工作流，而不是创建多个活动或优惠，并改变模板不同部分的投放。
* 使您能够创建、管理和批准优惠，而不是Adobe Campaign标准电子邮件活动工作流程。
* 控制在电子邮件优惠和客户中显示活动的次数。

## 访问优惠 {#task_DEB6F6A4B6E04E15AD3E1817D700688E}

了解如何访问优惠管理。

1. 请联系Adobe以获取配置信息。

   Experience Cloud组织必须具有Campaign Standard实例。 Adobe还可以在活动中启用一项功能，以便您在电子邮件中创建优惠活动。

1. 从Experience Cloud导航菜单中，单击解决方案选择器，然后单击 **[!UICONTROL 优惠]**。

   ![](assets/access-offers.png)

   要访问Campaign Standard中的优惠，请单击电子 **[!UICONTROL 邮件模板]** 中的优惠图标。

   ![](assets/campaign-add-offer.png)

   在Marketing Cloud中和您的Adobe Campaign帐户中看到这两个项目后，您便可以开始使用必要的功能。

## Users and Permissions {#concept_81F0ABB07ACC49E099EDCD87AA0436E1}

管理员可以在Admin Console中将用 [!UICONTROL 户添加到优惠] 管理中。 系统会向新用户发送电子邮件邀请，其中包含有关访问产品的说明。 添加用户后，您可以调整其权限，使他们能够在整个优惠管理中访问不同 [!UICONTROL 的功能]。

有关使用Admin Console的详细信息，请参阅 [HelpX Admin Console文档](https://helpx.adobe.com/enterprise/help/aedash.html)。

在活动中，标准用户自动有权将优惠活动嵌入电子邮件模板中。

>[!NOTE]
>
>对于测试版，没有相应的权限。 已添加到优惠的每个用户都可以完全访问优惠管理中的所 [!UICONTROL 有功能]。

## 为优惠管理创建产品用户档案

产品用户档案是一组权限，可以组合这些权限在产品中创建用户角色。 必须创建产品用户档案，然后将用户或用户组分配给他们。

1. 导航到Adobe [Admin Console](https://adminconsole.adobe.com/)。

1. 单击您的流程(**[!UICONTROL 例如]**,优惠)。

1. 在“产 [!UICONTROL 品用户档案] ”页面上，单 **[!UICONTROL 击“新用户档案”]**。

1. 键入产品用户档案的名称和说明，然后单击“完 **[!UICONTROL 成”]**。

1. 单击&#x200B;**[!UICONTROL 保存]**。

### 权限——定义

A description of [!UICONTROL 优惠管理] , [!UICONTROL Admin Console]in the product 用户档案可用的权限。

| 元素 | 描述 |
|--- |--- |
| 创建和编辑优惠 | 允许用户在优惠管理中创建和编辑 [!UICONTROL 优惠]。 如果用户具有此权限，但没有“批准 _优惠_ ”权限，则用户只能创建优惠并提交它进行批准。 在优惠活动获得批准前，不得在协议中使用。 |
| 删除优惠 | 允许用户删除优惠。 |
| 批准优惠 | 允许用户批准优惠。 如果任何优惠需要批准，具有此权限的用户将在登录到优惠管理时看到通知。 如果用户同时具有此权限和创建和编 _辑优惠权限_ ，则可以在单个工作流中创建和批准优惠。 |
| 存档优惠 | 使用户能够存档优惠。 |
| 创建标签 | 使用户能够在“标签”选项卡中和优惠创建屏幕中串联创建标签。 如果没有此权限，用户在创建优惠时只能选择预先创建的优惠。 |
| 编辑标签 | 允许用户编辑“标签”选项卡中的标签。 |
| 删除标签 | 允许用户在“标签”选项卡中删除标签。 |
| 创建版面 | 允许用户在“版面”选项卡中创建版面。 |
| 编辑位置 | 允许用户在“版面”选项卡中编辑版面。 |
| 删除位置 | 允许用户删除“版面”选项卡中的版面。 **注意：** 只能删除优惠活动中未使用的位置。 |