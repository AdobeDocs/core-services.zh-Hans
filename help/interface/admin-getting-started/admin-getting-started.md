---
description: 了解有关登录到 Admin Console 并管理 Experience Cloud 用户权限和产品配置文件，以及浏览器支持的信息。
keywords: core services
seo-description: 了解有关登录到 Admin Console 并管理 Experience Cloud 用户权限和产品配置文件，以及浏览器支持的信息。
seo-title: 管理 Experience Cloud 用户和产品
solution: Experience Cloud
title: 管理 Experience Cloud 用户和产品
index: true
translation-type: ht
source-git-commit: 01277057733cb921ebfbb7e66a3e34cdd1e21829
workflow-type: ht
source-wordcount: '1455'
ht-degree: 100%

---


# 管理 Experience Cloud 用户和产品 {#topic_3FCB4099640647E3B2411ADBFCE81909}

了解有关登录到 Admin Console 并管理 Experience Cloud 用户权限和产品配置文件，以及浏览器支持的信息。

>[!IMPORTANT]
>
>在 Admin Console 中管理用户会引入新的术语、界面和导航。以下信息介绍了这些变化，并且提供了指向其他帮助资源的链接。该帮助补充了 Adobe 所有云产品的[《企业管理用户指南》](https://helpx.adobe.com/cn/enterprise/managing/user-guide.html)中的信息。

## Experience Cloud 用户管理中的新增功能 {#concept_06A0A13362F644FB90F947238407637A}

了解 Experience Cloud 用户管理的最新功能。

<!-- ### Business ID type

Adobe is introducing an identity type called _Business ID_. This identity type improves the control of user and product management. Adobe is migrating all Adobe IDs (owned by individuals) that are used for business to the new enterprise Business IDs owned by your organization.

If you are an existing Experience Cloud customer, Adobe will migrate all your users on the Admin Console with Adobe IDs to Business IDs. If you are a new enterprise or teams customer, you will add users to the Admin Console using one of the available identity types: Business ID, Enterprise ID, or Federated ID.

Beginning May 2020, enterprise administrators cannot use the Adobe ID for new organizations created in the Admin Console. Latest: https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=engage&title=Type2e+DX+GTM

What to do

* Your users will need to accept Terms of Use (TOU) changes prior to accounts being migrated to Type2e. 
* Users that belong to multiple organizations might see a Profile Selection screen during the login workflow and need to select the correct one. This ensures that they are logging into the correct organization. (There might be multiple profiles to choose from if a users was a member of multiple organizations before the migration.) -->

### 管理工具

管理员可以在“管理工具”中查看所有 Experience Cloud 用户的可排序、可过滤列表及其详细信息。请参阅[在管理工具中查看 Experience Cloud 用户](admin-tool-experience-cloud.md)。

## 登录到 Admin Console {#section_705072FD4EBE4B70BC69EC81F2BB8669}

管理员不再管理解决方案中的用户。Experience Cloud 的用户和产品管理现在在 Admin Console 中进行。

要登录 Admin Console，请执行以下操作：

1. 导航到 [https://adminconsole.adobe.com/enterprise/](https://adminconsole.adobe.com/enterprise/#)。
1. 键入您的 [Adobe ID 或 Enterprise ID](https://helpx.adobe.com/cn/enterprise/help/identity.html) 和密码。

或者，从 Experience Cloud 菜单 (![](assets/menu-icon.png)) 中，单击&#x200B;**[!UICONTROL 管理]** > **[!UICONTROL 启动 Admin Console]**。

**相关帮助**

Creative Cloud 和 Document Cloud 的[管理用户指南](https://helpx.adobe.com/cn/enterprise/using/users.html)。某些信息与 Experience Cloud 用户管理相关，例如[管理身份类型](https://helpx.adobe.com/cn/enterprise/help/identity.html)。

[登录并管理配置文件设置](../admin-getting-started/getting-started-experience-cloud.md#topic_AC564B6795334DE39359ADD87F52F2E0)，以管理密码、组织和通知。

## 产品配置文件和组 {#section_AB50558124D541CF80A0D3D76D35A4BF}

产品配置文件的添加标志着以前管理解决方案产品和服务的方式（通过使用组）发生了转变。在 Admin Console 中，权限基于产品配置文件，即您可以分配给用户的产品和服务组。

例如，在 Analytics 中，您可以配置报表工具集合（如 Analysis Workspace 和 Report Builder）以及报表包、量度、维度等。您可以通过将用户添加到产品配置文件来授予其对产品配置文件的权限。请参阅[将 Analytics 访问权限分配给产品配置文件](../admin-getting-started/admin-getting-started.md#task_040673FE3E3E429B9531FBCB8B6A4391)。

**相关帮助**

[授权有限的管理权限](../admin-getting-started/admin-getting-started.md#task_3A072C4AA9734BC59FFA7E015271BC7E)

## Analytics {#section_97DE101F92CD494AB073893680992F1A}

在 Admin Console 中管理 Analytics 用户和产品权限。

[将 Analytics 访问权限分配给产品配置文件](../admin-getting-started/admin-getting-started.md#task_040673FE3E3E429B9531FBCB8B6A4391)（在此页面上）。

**用户帐户迁移**

Analytics 用户 ID 迁移工具可帮助 Analytics 管理员将用户帐户从 Analytics 用户管理迁移到 [Adobe Admin Console](https://adminconsole.adobe.com/enterprise/)。

Adobe 正在分阶段向客户推出这项帐户迁移功能。当您需要将现有用户帐户从&#x200B;**[!UICONTROL 管理工具]** > **[!UICONTROL 用户管理]**&#x200B;迁移到 Admin Console 时，Adobe 会通知您并给予协助。

迁移后，用户在 [experiencecloud.adobe.com](https://experiencecloud.adobe.com) 上使用他们的 Adobe ID（或 Enterprise ID）登录，并对其 Experience Cloud 解决方案和服务进行身份验证。如果用户尝试通过旧版的登录方式（[!DNL my.omniture.com] 和 [!DNL sc.omniture.com]）进行登录，则会被重定向至 [!DNL experiencecloud.adobe.com]。

**相关帮助**

[Analytics 用户 ID 迁移](https://docs.adobe.com/content/help/zh-Hans/analytics/admin/user-product-management/user-management/migrate-users/c-migration-tool.html)

## Adobe Target - 产品配置文件与工作区 {#section_3860AF177C9E4C7E9C390D36A414F353}

在 Adobe Target 中，工作区就是产品配置文件。它允许组织为一组特定用户分配一组特定属性。在很多方面，工作区与 Adobe Analytics 中的报表包类似。

请参阅：
* [企业用户权限](https://docs.adobe.com/content/help/zh-Hans/target/using/administer/manage-users/enterprise/property-channel.html)
* [管理产品和配置文件](https://helpx.adobe.com/cn/enterprise/using/manage-products-and-profiles.html)
* 视频：[如何在 Adobe Admin Console 中配置 Adobe Target 工作区](https://helpx.adobe.com/cn/target/kb/how-to-configure-target-workspaces-in-adobe-admin-console0.html)

## Campaign - 产品配置文件、租户和安全群组 {#section_09CDF75366444CF5810CF321B7C712F3}

Campaign 中的&#x200B;*租户*&#x200B;在 Admin Console“产品”页面上显示为&#x200B;*产品*。

*安全组*&#x200B;显示为产品配置文件。

有关安全组以及将用户分配给安全组的信息，请参阅[管理组和用户](https://helpx.adobe.com/cn/campaign/standard/administration/using/managing-groups-and-users.html)。

## Experience Platform Launch {#section_F2DA6778DD2D48AA8F794041971EE6B1}

Experience Platform Launch 会显示在 Admin Console 的“产品”页面上。您可以在 Launch 产品配置文件中包含其他解决方案和服务。

有关 Admin Console 中用户权限以及设置特定于 Launch 的选项（包括为配置文件分配权限）的信息，请参阅[用户管理](https://docs.adobelaunch.com/launch-reference/administration/user-permissions)。

## Experience Manager 云服务

Adobe 企业客户在 Adobe Admin Console 中表示为 IMS 组织。这是 Adobe 客户管理其用户和组的产品权利的门户。AEM 客户可以使用 Adobe Admin Console 管理其产品权利以及对 AEM 云服务的 IMS 身份验证。

请参阅 [AEM 云服务的 IMS 支持](https://docs.adobe.com/content/help/zh-Hans/experience-manager-cloud-service/security/ims-support.html#managing-products-and-user-access-in-admin-console)。

## 动态标签管理器 {#section_3A41CF2BD5994B9891537D063571D4ED}

您可以邀请用户使用 Dynamic Tag Management、分配用户角色和将用户添加到群组。

有关如何邀请用户使用 Dynamic Tag Management、分配用户角色以及将用户添加到群组的信息，请参阅[用户和权限](https://docs.adobe.com/content/help/zh-Hans/dtm/using/admin/users.html)。

## Audience Manager {#section_C31E3FA8A1E14463B1B3E07235F1983C}

创建 Audience Manager 用户并将其分配给组。您还可以查看限制（特征、区段、目标和 [!DNL AlgoModel]）。

请参阅 Audience Manager 帮助中的[管理](https://docs.adobe.com/content/help/zh-Hans/dtm/using/admin/users.html)。

## 管理 Experience Cloud 产品 {#task_16335111C52D40E9BAC73D0699584DBF}

创建产品配置文件，并将其分配给权限组。

邀请用户加入组织时，您可以授予用户访问产品和产品配置文件的权限。您还可以将有限的管理权限委派给某个用户。同样，您可以创建用户组，然后将该组添加到产品配置文件以启用访问权限。

1. 在 [Admin Console](https://adminconsole.adobe.com/enterprise/) 中，单击&#x200B;**[!UICONTROL 产品]**。
1. 单击&#x200B;**[!UICONTROL 新建配置文件]**。
1. 配置该配置文件的详细信息，然后单击&#x200B;**[!UICONTROL 下一步]**。
1. 单击&#x200B;**[!UICONTROL 完成]**。

有关更多帮助，请访问：

* [管理产品和配置文件](https://helpx.adobe.com/cn/enterprise/using/manage-products-and-profiles.html)
* 有关更多信息，请参阅 Adobe Target 帮助中的[企业用户权限](https://docs.adobe.com/content/help/zh-Hans/target/using/administer/manage-users/enterprise/property-channel.html)。
* 视频：[如何在 Adobe Admin Console 中配置 Adobe Target 工作区](https://helpx.adobe.com/cn/target/kb/how-to-configure-target-workspaces-in-adobe-admin-console0.html)

## 将 Analytics 访问权限分配给产品配置文件 {#task_040673FE3E3E429B9531FBCB8B6A4391}

将 Analytics 报表访问权限（报表包、量度、维度等）分配给产品配置文件。

例如，您可以创建一个产品配置文件，其中包含多个 Analytics 工具（[!UICONTROL Analysis Workspace]、[!UICONTROL Reports &amp; Analytics] 和 [!UICONTROL Report Builder]），然后为其分配用来访问特定量度和维度（包括 eVar）以及创建区段或计算量度等功能的权限。

1. 登录到 [Admin Console](https://adminconsole.adobe.com/enterprise)，然后单击&#x200B;**[!UICONTROL 产品]**（或单击您的产品名称）。
1. 随后，在产品配置文件中，单击&#x200B;**[!UICONTROL 权限]**（只有管理员才能使用）。
1. 配置该配置文件的权限：

| 元素 | 描述 |
|--- |--- |
| Report Suites | 启用对特定报表包的权限。 |
| 量度 | 启用流量、转化、自定义事件、解决方案事件和内容识别等的权限。 |
| 维度 | 在粒度级别自定义用户访问权限，包括 eVar、流量报表、解决方案报表和路径报表。 |
| 报表包工具 | 启用 Web 服务、报表包管理、工具和报表及功能板项目的用户权限。 |
| Analytics 工具 | 启用常规项目（帐单、日志等）、公司管理、工具、Web 服务访问、Report Builder 和 Data Connectors 集成的用户权限。“自定义 Admin Console”类别中的“公司设置”已被移动到“Analytics 工具”中。 |

## 将管理角色分配给用户 {#task_3A072C4AA9734BC59FFA7E015271BC7E}

在 Admin Console 中，您可以将有限的管理权限委派给贵组织中的其他人员。凭借委派的角色，用户能够管理对最终用户的软件访问权限，提供访问部署功能，并充当支持代表。

例如，您可以：

* 允许您的创意总监授予对 Creative Cloud 的访问权限。
* 允许您的营销总监授予对 Experience Cloud 的访问权限。
* 将这两个角色分开，以便它们不会逾越彼此的角色权限。

通过使用这些角色，您可以将管理同时委派给其他人，而不会提供超出其需求的更多功能。

1. 在 Admin Console 中，单击&#x200B;**[!UICONTROL 用户]**，然后单击用户的名称。
1. 单击&#x200B;**[!UICONTROL 编辑管理权限]**。
1. 配置用户的管理权限。
1. 单击&#x200B;**[!UICONTROL 下一步]**&#x200B;以查看设置，然后单击&#x200B;**[!UICONTROL 保存]**。

## 支持的浏览器和系统要求 {#concept_CDC4371EB9BF433E9534F8716DC8A088}

Experience Cloud 中支持的浏览器。

* [!DNL Microsoft Edge]（Microsoft 已[结束](https://www.microsoft.com/zh-cn/WindowsForBusiness/End-of-IE-support)对 Internet Explorer 8、9 和 10 的支持。因此，Adobe 将不会针对这些特定 Internet Explorer 版本报告的问题进行修复。）
* [!DNL Google Chrome]
* [!DNL Firefox]
* [!DNL Safari]
* [!DNL Opera]

**注意：**&#x200B;尽管 Experience Cloud 界面支持这些浏览器，但单个解决方案可能不会支持每个浏览器。（例如，[Analytics](https://docs.adobe.com/content/help/zh-Hans/analytics/admin/sys-reqs.html) 不支持[!DNL Opera]，[Adobe Target](https://docs.adobe.com/help/zh-Hans/target/using/implement-target/before-implement/supported-browsers.html) 不支持[!DNL Safari]。）

### 解决方案和产品要求

* [Analytics](https://docs.adobe.com/content/help/zh-Hans/analytics/admin/sys-reqs.html)
* [Report Builder](https://docs.adobe.com/content/help/zh-Hans/analytics/analyze/report-builder/report-builder-setup/system-requirements.html)
* [Adobe Target](https://docs.adobe.com/help/zh-Hans/target/using/implement-target/before-implement/supported-browsers.html)
