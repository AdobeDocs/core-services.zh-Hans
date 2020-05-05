---
description: 了解如何将一个或多个报表包映射到组织。
seo-description: 了解如何将一个或多个报表包映射到组织。
seo-title: 将报表包映射到组织
title: 将报表包映射到组织
uuid: b983d5a6-b3d0-4137-ac53-bc5681d3e58b
translation-type: tm+mt
source-git-commit: 08e8e5fea4e4e64a195ebe25ae3ef19e849cabc5

---


# 将报表包映射到组织 {#topic_7C4740559EAC4E0FA5F8DEF886B580DA}

了解如何将一个或多个报表包映射到组织。

<!-- May 5 2020: This feature will likely be deprecated in Nov 2020. Any users with outstanding report suites that are not mapped will have 6 months to map their RS. -->

Experience Cloud服务(如Experience Cloud ID服务和人 [!UICONTROL 员])与组织而不是单个报表包相关联。 要确保这些服务能够正确运行，必须将每个Analytics报表包映射到一个组织。 映射过程：

* 将Experience Cloud组织设置为报表包的主组织。
* 不更改谁可以访问报表包（访问权限仍由每个用户的Adobe Analytics登录帐户决定）

## 要求

您必须是登录公司的Analytics管理员，该管理员有权访问要映射的报表包。 此外，此帐户必 [须链接到Experience Cloud组织](../admin-getting-started/organizations.md#topic_C31CB834F109465A82ED57FF0563B3F1) ，才能将报表包映射到该组织。

如果您不具备组织下对给定报表包拥有访问权限的登录公司的 Analytics 管理员权限，则组织将呈灰显状态。

## 将一个报表包映射到组织 {#task_23993FE78DF6455FA8D7BE60686EA16C}

1. Click **[!UICONTROL Experience Cloud]** > **[!UICONTROL Administration]** > **[!UICONTROL Report Suite Mapping]**

1. 要查看对每个报表包拥有访问权限的登录公司，请单击&#x200B;**[!UICONTROL 对登录公司可见]**。

   此视图可帮助您针对映射做出明智决定。

1. 单击报表包旁边&#x200B;**[!UICONTROL 已映射的组织]**&#x200B;列中的下拉菜单，然后选择要映射到的组织。

   有关选择 Experience Cloud 组织的提示，请参阅下一部分。

## 将多个报表包映射到组织 {#task_94955B0D8ABA4CB1A38746ECF8E32711}

1. Click **[!UICONTROL Experience Cloud]** > **[!UICONTROL Administration]** > **[!UICONTROL Report Suite Mapping]**.

1. 选择要映射的报表包。

   ![](assets/rs-mapping-multiple.png)

1. 选择组织（在此示例中为 Outdoors Inc），然后单击&#x200B;**[!UICONTROL 选择]**。

   有关选择 Experience Cloud 组织的提示，请参阅下一部分。

1. 单击&#x200B;**[!UICONTROL 保存映射]**。

## 关于选择 Experience Cloud 组织的提示 {#mapping-tips}

本节包含一些提示，可帮助您选择应将报表包映射到的Experience Cloud组织。

### 我应选择哪个组织？

If the Experience Cloud ID Service is currently deployed on the report suite, ensure the organization you select in the Report Suite Mapping tool is the same organization specified in the [!DNL visitorAPI.js] file on your site. You can use the instructions in [Test and Verify the Experience Cloud ID Service](https://docs.adobe.com/content/help/en/id-service/using/implementation-guides/test-verify.html) to find the org ID that is being used by the Visitor ID service.

如果访客ID服务尚未部署在为报表包收集数据的站点上，则如果您将来部署Experience Cloud访客ID服务，您需要确保您的部署与您在报表包映射工具中选择的组织匹配。

### 为什么某些组织灰显？

这表示您没有足够的权限映射到灰显的报表包。 请仔细研究下面的示例：

![](assets/rs-mapping.png)

在此图表中，蓝色钥匙表示管理员权限。灰线表示可见性。

此用户有权访问两个Experience Cloud组织。 他进行了以下工作：

* 将他在Chapek Analytics登录公司 [!UICONTROL 中的] admin帐户关联 [!UICONTROL 到他的] Chapek Corp Experience Cloud组织帐户。
* 将他在Doohan Analytics登录公司 [!UICONTROL 中的] 非管理员帐户关 [!UICONTROL 联到] 其Chapek Corp Experience Cloud组织帐户。
* 在奈杰尔分析登录公司将他的非管理员帐户与他的奈杰尔公司Experience Cloud组织帐户关联。

以下点列表了此用户可以和不能对这些报表包执行的映射操作：

* [!UICONTROL Chapek-prod报表包] 可映射到Chapek [!UICONTROL Corp组织，因为此用户是链接的Analytics登录公司(] Chapek)的管理员，且其帐户已链接到此组织。
* [!UICONTROL 此用户无法链接] nigel-prod报告套件，因为他不是任何登录公司的管理员，而此报告套件可见。
* [!UICONTROL Doohan-prod报表包] 可映射到 [!UICONTROL Chapek Corp] ，因为此用户是链接到Experience Cloud组织的登录公司([!UICONTROL Chapek])的管理员(请注意，他不是Doohan Analytics登录公司的管理员)。 必须注意，Doohan-prod报 [!UICONTROL 告套件也有资格被映射到Nigel Inc] Experience Cloud组织，尽管此用户无法执行该映射。 在这种情况下，Experience Cloud的两个组织都会显示在列表中，但 [!UICONTROL Nigel Inc] 灰显。 在绘制地图之前，该用户应咨询奈杰尔登录公司的管理员，以确定哪个组织最适合绘制地图。 如果您选择的组织与最初创建报表包的组织不同，则UI会显示“可能的冲突”警告。

## 常见问题解答 {#section_099E485805994C929FF9C9F75219BEE1}

### 为何看不到所有报表包？

您的某些报表包可能在其他登录公司下显示。 您可以使用屏幕顶部的下拉菜单更改当前登录公司。

### 如果我无法识别某个报表包下拉列表中列出的某些组织，该怎么办？

The list shows you all the *possible* organizations your report suite could be mapped to, even you don’t have permission to map to all those report suites. 如果您不确定该报表包是否应映射到该列表中一个灰显的报表包，请咨询您组织中的Experience Cloud管理员，以确定最佳选择。

### 如果我无法识别“登录公司可见”列中为报表包列出的登录公司，该怎么办？

某时，此报表包已与另一个登录公司共享，该登录可能是其他Experience Cloud组织的一部分。

### 关于由其他组织生成的报表包的“可能冲突”错误是什么？ 为什么这很重要？

这是一条通知，可帮助您对报表包映射做出明智决策。 我们希望您知道报表包最初是在其他组织下创建的，以防组织可能更适合此报表包。

### 如何知道报表包是否已映射？

映射的报表包将以不可编辑的格式显示。 如果您需要更改映射，请联系客户关怀。

### 如果我只知道Experience Cloud组织的组织ID怎么办？ 如何查找我的组织 ID 的名称？

您可以在“组织和帐户设置” [中找到您的组织名称](https://docs.adobe.com/content/help/zh-Hans/core-services/interface/manage-users-and-products/organizations.html)。

### 我在“映射日期”列中看到一个日期。 谁绘制了地图？

您可以参考分析界面中的报表包更改日志，以检查进行更改的用户ID。 查找事件“与IMS组织关联的套件”。
