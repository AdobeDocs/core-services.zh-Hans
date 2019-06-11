---
description: 了解如何将一个或多个报表包映射到组织。
seo-description: 了解如何将一个或多个报表包映射到组织。
seo-title: 将报表包映射到组织
title: 将报表包映射到组织
uuid: b983d5a6-b3 d0-4137-ac53-bc5681 d3 e58 b
translation-type: tm+mt
source-git-commit: d9d6cebc0e9e14eac2471dc79b91276a154e35e0

---


# 将报表包映射到组织 {#topic_7C4740559EAC4E0FA5F8DEF886B580DA}

了解如何将一个或多个报表包映射到组织。

Experience Cloud 服务（例如，Experience Cloud ID 服务和“人员”核心服务）与某个组织（而非单个报表包）相关联。要确保这些服务能够正常运行，必须将每个 Analytics 报表包映射到组织。映射流程：

* 将 Experience Cloud 组织设置为报表包的主要组织。
* 请勿更改对报表包拥有访问权限的用户（访问权限仍取决于每个用户的 Adobe Analytics 登录帐户）


**要求**

您必须是对要映射的报表包拥有访问权限的登录公司中的 Analytics 管理员。此外，要将报表包映射到 Experience Cloud 组织，这个帐户还必须[与 Experience Cloud 组织关联](../admin-getting-started/organizations.md#topic_C31CB834F109465A82ED57FF0563B3F1)。

如果您不具备组织下对给定报表包拥有访问权限的登录公司的 Analytics 管理员权限，则组织将呈灰显状态。

## 将报表包映射到组织 {#task_23993FE78DF6455FA8D7BE60686EA16C}

1. 单击 **[!UICONTROL Experience Cloud]** &gt; **[!UICONTROL 管理]** &gt; **[!UICONTROL 报表包映射]**

   您还可以使用[直接 URL](https://audience.marketing.adobe.com/rsmapping/ui.html)。

1. 要查看有权访问每个报告套件的登录公司，请单击 **[!UICONTROL 登录公司可见]**。

   此视图可帮助您针对映射做出明智决定。

1. 单击报表包旁边 **[!UICONTROL 已映射的组织]列中的下拉菜单，然后选择要映射到的组织。**

   有关选择Experience Cloud组织的提示，请参阅下一节。

## 将多个报表包映射到一个组织 {#task_94955B0D8ABA4CB1A38746ECF8E32711}

1. 单击 **[!UICONTROL “Experience Cloud]** ”&gt;“ **[!UICONTROL 管理]** ”&gt; **[!UICONTROL “报表包映射]**”。

   您还可以使用[直接 URL](https://audience.marketing.adobe.com/rsmapping/ui.html)。

1. 选择要映射的报表包。

   ![](assets/rs-mapping-multiple.png)

1. 选择组织(Outdoors Inc，在本例中)，然后单击 **[!UICONTROL 选择]**。

   有关选择Experience Cloud组织的提示，请参阅下一节。

1. 单击 **[!UICONTROL “保存映射]**”。

## 关于选择 Experience Cloud 组织的提示 {#mapping-tips}

此部分提供的提示可帮助您选择应该将报表包映射到的 Experience Cloud 组织。

**我应该选择哪个组织？**

如果当前已在报表包上部署 Experience Cloud ID 服务，请确保您在报表包映射工具中选择的组织与在您网站上的 [!DNL visitorAPI.js] 文件中指定的组织相同。您可以按照[测试和验证 Experience Cloud ID 服务](https://marketing.adobe.com/resources/help/en_US/mcvid/mcvid-test-verify.html)中的说明来查找访客 ID 服务所使用的组织 ID。

如果为报表包收集数据的网站上尚未部署访客 ID 服务，那么当您将来部署 Experience Cloud 访客 ID 服务时，您将需要确保部署中的组织与您在报表包映射工具中选择的组织一致。

**为什么有些组织呈灰显状态？**

这种情况表示您没有足够的权限来映射到灰显的报表包。请仔细研究下面的示例：![](assets/rs-mapping.png)在此图表中，蓝色钥匙表示管理员权限。灰色线条表示可见性。

此用户对两个 Experience Cloud 组织拥有访问权限。他执行了以下操作：

* 将其在 Chapek Analytics 登录公司中的管理员帐户与其 Chapek Corp Experience Cloud 组织帐户相关联。
* 将其在 Doohan Analytics 登录公司中的非管理员帐户与其 Chapek Corp Experience Cloud 组织帐户相关联。
* 将其在 Nigel Analytics 登录公司中的非管理员帐户与其 Nigel Inc Experience Cloud 组织帐户相关联。

以下几点列出了此用户针对这些报表包可以执行以及无法执行的映射操作：

* Chapek-prod 报表包可以映射到 Chapek Corp 组织，因为此用户是已关联的 Analytics 登录公司 (Chapek) 的管理员，并且其帐户已与该组织相关联。
* Nigel-prod 报表包无法由此用户进行关联，因为他不是可查看此报表包的任何登录公司的管理员。
* Doohan-prod 报表包可以映射到 Chapek Corp，因为此用户是已与 Experience Cloud 组织关联的登录公司 (Chapek) 的管理员（请注意，他并不是 Doohan Analytics 登录公司的管理员）。请务必注意，Doohan-prod 报表包也可以映射到 Nigel Inc Experience Cloud 组织，尽管此用户无法执行该映射。在此示例中，两个 Experience Cloud 组织都显示在列表中，但 Nigel Inc 呈灰显状态。在映射之前，此用户应咨询 Nigel 登录公司的管理员，以确定哪个组织是映射的最佳选项。如果您选择的组织与报表包最初创建时所在的组织不一致，UI 将显示可能存在冲突的警告。

## 常见问题解答 {#section_099E485805994C929FF9C9F75219BEE1}

**为什么我看不到我的所有报表包？**

您的一些报表包可能显示在其他登录公司下。您可以使用屏幕顶部的下拉菜单更改当前的登录公司。

**如果在我的某个报表包的下拉菜单中列出的有些组织我不认识，该怎么办？**

该列表向您显示可能会映射到报表包的所有*可能的*组织，即使您没有映射到所有这些报表包的权限。如果您不确定是否应将报表包映射到列表中的某个灰显组织，请咨询贵组织中的 Experience Cloud 管理员，以确定最佳选项。

**在“对登录公司可见”列中为报表包列出的有些登录公司我不认识，这是怎么回事？**

有时，此报表包已共享给另一个登录公司，而该登录公司属于其他 Experience Cloud 组织。

**与由其他组织生成的报表包相关的“可能存在冲突”错误是什么？这为什么很重要？**

这个错误是一个通知，可帮助您针对报表包映射做出明智决定。我们希望您能了解该报表包最初是在其他组织下创建的，有可能该组织是更适合此报表包的选项。

**如何了解是否已映射某个报表包？**

已映射的报表包会以不可编辑的格式显示。如果您需要更改映射，请联系客户关怀团队。

**如果我只知道自己的 Experience Cloud 组织的组织 ID，该怎么办？如何查找我的组织 ID 的名称？**

您可以在[组织和帐户设置](https://marketing.adobe.com/resources/help/en_US/mcloud/?f=organizations)中找到您的组织名称。

**我在“映射日期”列中看到一个日期。是谁执行的该映射？**

您可以在 Analytics 界面中查阅“报表包更改日志”，以查看执行该更改的用户 ID。可查找事件“Suite associated to IMS Organization”。
