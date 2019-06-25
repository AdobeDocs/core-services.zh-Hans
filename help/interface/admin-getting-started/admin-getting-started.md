---
description: 了解如何登录到 Admin Console 并管理 Experience Cloud 用户权限和产品配置文件。
keywords: 核心服务
seo-description: 了解如何登录到 Admin Console 并管理 Experience Cloud 用户权限和产品配置文件。
seo-title: 管理 Experience Cloud 用户和产品
solution: Marketing Cloud
title: 管理 Experience Cloud 用户和产品
uuid: aea4e4c3-f543-4e8d-b553-d838418477d6
translation-type: ht
source-git-commit: 979b2202a70e2a5362aa86a65a17d7c4279b3a1a

---


# 管理 Experience Cloud 用户和产品 {#topic_3FCB4099640647E3B2411ADBFCE81909}

了解如何登录到 Admin Console 并管理 Experience Cloud 用户权限和产品配置文件。


<!-- marketing-cloud-identity-management.xml -->

<!-- user_mgmt_admin.xml -->

<!-- domain change for 2018 
<ul id="ul_6654B3993EBE4DE0A3FBCFA5173A52D1"> 
 <li id="li_BE41EB31960B4C079E864FAA2E322BB4"> Private Beta - Support new domain alongside old domain for selected customers (June, 2018) </li> 
 <li id="li_0513CA457FAA4F37A9D5E514DEAF2067"> General Rollout - Serve both old and new domains seamlessly for all customers (Aug, 2018) </li> 
 <li id="li_AB89A6D00A274EB7863D0243757322DE"> Public Beta - Drive solution teams and customers to switch references from old domain to new domain (Aug - Oct, 2018) </li> 
 <li id="li_6FED48B1F361493082102E823EA335F4"> General Availability - Redirect all old domain requests to new domain (Oct, 2018) </li> 
</ul> -->

>[!IMPORTANT]
>
>在 Admin Console 中管理用户会引入新的术语、界面和导航。以下信息介绍了这些变化，并且提供了指向其他帮助资源的链接。该帮助补充了 Adobe 所有云产品的[《企业管理用户指南》](https://helpx.adobe.com/cn/enterprise/managing/user-guide.html)中的信息。

## Experience Cloud 用户管理中的新增功能 {#concept_06A0A13362F644FB90F947238407637A}

了解 Experience Cloud 用户管理的最新功能。


## 登录到 Admin Console {#section_705072FD4EBE4B70BC69EC81F2BB8669}

在解决方案中，管理员不再管理用户。现在，Experience Cloud 的用户和产品管理均在 Admin Console 中进行。

**要登录到 Admin Console**，请执行以下操作：

1. 导航到 [https://adminconsole.adobe.com/enterprise/](https://adminconsole.adobe.com/enterprise/#)。
1. 键入您的 [Adobe ID 或 Enterprise ID](https://helpx.adobe.com/cn/enterprise/using/identity.html￼) 和密码。


或者，从 Experience Cloud 菜单 (![](assets/menu-icon.png)) 中，单击 **[!UICONTROL 管理]** &gt; **[!UICONTROL 启动 Admin Console]**。

**相关帮助**

适用于 Creative Cloud 和 Document Cloud 的[管理用户指南](https://helpx.adobe.com/cn/enterprise/using/users.html)。某些信息与 Experience Cloud 用户管理相关，例如[管理身份类型](https://helpx.adobe.com/cn/enterprise/using/identity.html)。

通过[登录并管理您的配置文件设置](../admin-getting-started/getting-started-experience-cloud.md#topic_AC564B6795334DE39359ADD87F52F2E0)，来管理密码、组织和通知。

## 产品配置文件和群组 {#section_AB50558124D541CF80A0D3D76D35A4BF}

增加产品配置文件意味着以往管理解决方案产品及服务的方式（通过使用群组）发生转变。在 Admin Console 中，权限基于产品配置文件，而产品配置文件则涵盖了若干组可以分配给用户的产品和服务。

举例来说，在 Analytics 中，您可以配置一系列报表工具，例如 Analysis Workspace 和 Report Builder，以及报表包、量度、维度等。通过将这些工具添加到配置文件，您可以向用户授予该产品配置文件的权限。请参阅 [将 Analytics 访问权限分配给产品配置文件](../admin-getting-started/admin-getting-started.md#task_040673FE3E3E429B9531FBCB8B6A4391).

**相关帮助**

[授权有限的管理权限](../admin-getting-started/admin-getting-started.md#task_3A072C4AA9734BC59FFA7E015271BC7E)

## Analytics {#section_97DE101F92CD494AB073893680992F1A}

在 Admin Console 中管理 Analytics 用户和产品权限。

[将 Analytics 访问权限分配给产品配置文件](../admin-getting-started/admin-getting-started.md#task_040673FE3E3E429B9531FBCB8B6A4391)（在此页面上）。

**用户帐户迁移**

Analytics 用户 ID 迁移工具可帮助 Analytics 管理员将用户帐户从 Analytics 用户管理迁移到 [Adobe Admin Console](https://adminconsole.adobe.com/enterprise/)。

Adobe 正在分阶段向客户推出这项帐户迁移功能。当您需要将现有用户帐户从 **[!UICONTROL 管理工具]** &gt; **[!UICONTROL 用户管理]** 迁移到 Admin Console 时，Adobe 会通知您并给予协助。

迁移后，用户在 [marketing.adobe.com](https://marketing.adobe.com) 上使用他们的 Adobe ID（或 Enterprise ID）登录，并对其 Experience Cloud 解决方案和服务进行身份验证。如果用户尝试通过旧版的登录方式（[!DNL my.omniture.com] 和 [!DNL sc.omniture.com]）进行登录，则会被重定向至 [!DNL marketing.adobe.com]。

**相关帮助**

[Analytics 用户 ID 迁移](https://marketing.adobe.com/resources/help/zh_CN/experience-cloud/admin-console/analytics-migration/)

## Target - 产品配置文件与工作区 {#section_3860AF177C9E4C7E9C390D36A414F353}

在 Target 中，工作区就是产品配置文件。工作区允许组织向一组特定用户分配一组特定属性。在很多方面，工作区与 Adobe Analytics 中的报表包类似。

请参阅：
* [企业用户权限](https://marketing.adobe.com/resources/help/zh_CN/target/target/property_channel.html)
* [管理产品和配置文件](https://helpx.adobe.com/cn/enterprise/using/manage-products-and-profiles.html)
* 视频：[如何在 Adobe Admin Console 中配置 Target 工作区](https://helpx.adobe.com/cn/target/kb/how-to-configure-target-workspaces-in-adobe-admin-console0.html)




## Campaign - 产品配置文件、租户和安全群组 {#section_09CDF75366444CF5810CF321B7C712F3}

Campaign 中的*租户*会在“Admin Console 产品”页面中显示为*产品*。

*安全群组*会显示为产品配置文件。

有关安全群组和将用户分配给安全群组的信息，请参阅[管理群组和用户](https://helpx.adobe.com/cn/campaign/standard/administration/using/managing-groups-and-users.html)。

## Experience Platform Lauch {#section_F2DA6778DD2D48AA8F794041971EE6B1}

Experience Platform Lauch 会显示在 Admin Console 的“产品”页面上。您可以在 Launch 产品配置文件中包含其他解决方案和核心服务。

有关 Admin Console 中用户权限以及设置特定于 Launch 的选项（包括为配置文件分配权限）的信息，请参阅[用户管理](https://marketing.adobe.com/resources/help/zh_CN/experience-cloud/launch/user-management.html)。

## 动态标签管理器 {#section_3A41CF2BD5994B9891537D063571D4ED}

您可以邀请用户使用“动态标签管理”、分配用户角色和将用户添加到群组。

有关如何邀请用户使用 Dynamic Tag Management、分配用户角色以及将用户添加到群组的信息，请参阅[用户和权限](https://marketing.adobe.com/resources/help/zh_CN/dtm/users.html)。

## Audience Manager {#section_C31E3FA8A1E14463B1B3E07235F1983C}

创建 Audience Manager 用户并将其分配到群组。您还可以查看各种限制（特征、区段、目标和 AlgoModel）。

请参阅 Audience Manager 帮助中的[管理](https://marketing.adobe.com/resources/help/zh_CN/aam/c_administration.html)。

## 管理 Experience Cloud 产品 {#task_16335111C52D40E9BAC73D0699584DBF}

创建产品配置文件并将该文件分配给权限组。

当您邀请用户加入组织时，您可以授予用户访问产品和产品配置文件的权限。您还可以将有限的管理权限授权给用户。同样，您可以创建用户群组，然后将该群组添加到产品配置文件以启用访问。

1. 在 [Admin Console](https://adminconsole.adobe.com/enterprise/) 中，单击 **[!UICONTROL 产品]**。
1. 单击 **[!UICONTROL 新建配置文件]**。
1. 配置该配置文件的详细信息，然后单击 **[!UICONTROL 下一步]**。
1. 单击 **[!UICONTROL 完成]**。

以下资源提供了更多帮助：

* [管理产品和配置文件](https://helpx.adobe.com/cn/enterprise/using/manage-products-and-profiles.html)
* Target 帮助中的[企业用户权限](https://marketing.adobe.com/resources/help/zh_CN/target/target/property_channel.html)提供了更多信息。
* 视频：[如何在 Adobe Admin Console 中配置 Target 工作区](https://helpx.adobe.com/cn/target/kb/how-to-configure-target-workspaces-in-adobe-admin-console0.html)


## 将 Analytics 访问权限分配给产品配置文件 {#task_040673FE3E3E429B9531FBCB8B6A4391}

将 Analytics 报表访问权限（报表包、量度、维度等）分配给产品配置文件。

例如，您可以创建一个产品配置文件，其中包含多个 Analytics 工具（[!UICONTROL Analysis Workspace]、[!UICONTROL Reports &amp; Analytics] 和 [!UICONTROL Report Builder]），然后为其分配用来访问特定量度和维度（包括 eVar）以及创建区段或计算量度等功能的权限。

1. 登录到 [Admin Console](https://adminconsole.adobe.com/enterprise)，然后单击 **[!UICONTROL 产品]**（或单击您的产品名称）。
1. 随后，在产品配置文件中，单击 **[!UICONTROL 权限]**（只有管理员才能使用）。
1. 配置该配置文件的权限：


| 元素 | 描述 |
|--- |--- |
| 报表包 | 启用特定报表包的权限。 |
| 量度 | 启用流量、转化、自定义事件、解决方案事件和内容识别等的权限。 |
| 维度 | 在粒度级别自定义用户访问权限，包括 eVar、流量报表、解决方案报表和路径报表。 |
| 报表包工具 | 启用 Web 服务、报表包管理、工具和报表，以及功能板项目的用户权限。 |
| Analytics 工具 | 启用常规项目（帐单、日志等）、公司管理、工具、Web 服务访问、Report Builder 和 Data Connectors 集成的用户权限。“自定义 Admin Console”类别中的“公司设置”已被移动到“Analytics 工具”中。 |



## 将管理角色分配给用户 {#task_3A072C4AA9734BC59FFA7E015271BC7E}


<!-- t_admin-roles.xml -->
在管理控制台中，您可以将有限的管理权限分配给组织中的其他人员。通过分配的角色，用户可以管理最终用户的软件访问权限，提供访问部署功能，以及充当支持代表。

例如，您可以：

* 允许您的创意总监授予 Creative Cloud 的访问权限。
* 允许您的市场营销总监授予 Experience Cloud 的访问权限。
* 保持这两个角色相互独立，使他们二者之间无法逾越彼此的职责范围。


利用这些角色，您还可以同时向其他人员分配管理权限，而不提供超出其所需范围的更多职能。

1. 在 Admin Console 中，单击 **[!UICONTROL 用户]**，然后单击用户的名称。
1. 单击 **[!UICONTROL 编辑管理权限]**。
1. 配置用户的管理权限。
1. 单击 **[!UICONTROL 下一步]** 以查看设置，然后单击 **[!UICONTROL 保存]**。

## 支持的浏览器和系统要求 {#concept_CDC4371EB9BF433E9534F8716DC8A088}

Experience Cloud 中支持的浏览器。


<!-- browsers.xml -->
**Experience Cloud 核心服务**

* Microsoft 最新推出的 Internet Explorer。（对于 Internet Explorer 8、9 和 10，Microsoft 已[终止支持](https://www.microsoft.com/zh-cn/WindowsForBusiness/End-of-IE-support)。因此，Adobe 将不会修复针对这些特定 Internet Explorer 版本报告的问题。）
* Google Chrome
* Mozilla Firefox
* Apple Safari


**解决方案和产品要求**

* [Analysis Workspace 和 Reports &amp; Analytics](https://marketing.adobe.com/resources/help/zh_CN/sc/user/?f=requirements)（包括 Adobe Social）
* [Report Builder](https://marketing.adobe.com/resources/help/zh_CN/arb/system_requirements.html)
* [Ad Hoc Analysis](https://marketing.adobe.com/resources/help/zh_CN/dsc/c_sys_reqs.html)
* [Data Workbench](https://marketing.adobe.com/resources/help/zh_CN/insight/install/c_Data_Workbench_Client_install.html)
* [Adobe Target](https://marketing.adobe.com/resources/help/zh_CN/target/ov/?f=r_supported_browsers)
* [Adobe Audience Manager](https://marketing.adobe.com/resources/help/zh_CN/aam/?f=c_supported_browsers)
* [Adobe Campaign Standard](https://helpx.adobe.com/cn/campaign/standard/start/using/compatible-browsers.html)
* [Adobe Campaign Classic](https://helpx.adobe.com/cn/campaign/kb/compatibility-matrix.html)
