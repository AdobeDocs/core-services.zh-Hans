---
title: 用户和产品许可证管理
description: 在Admin Console中为Experience Cloud应用程序管理用户和产品许可证。
application: Experience Cloud
index: true
feature: Admin Console
topic: Administration
role: Admin
level: Experienced
exl-id: c82821c4-aa5d-48ae-8bef-5937fede8db2
source-git-commit: 77841faeb5b005e4913408edb3e9cfbbdfc8961d
workflow-type: tm+mt
source-wordcount: '728'
ht-degree: 5%

---

# 用户管理和产品许可证

本页提供了专门面向Experience Cloud管理员的信息，以及指向常用用户和产品管理文档的链接。

有关适用于所有Adobe应用程序的一般身份管理帮助，请参阅[企业和团队管理指南](https://helpx.adobe.com/cn/enterprise/admin-guide.html)。

## Admin Console中的管理角色

Admin Console提供三个主要管理角色，每个角色都具有特定的访问级别和责任级别：

| 角色 | 描述 |
| ------- | ------- |
| 系统管理员 | 完全访问 — 管理控制台的所有方面。 <br>主要职责： <br><ul><li>添加、删除和管理用户。</li><li>分配和撤销产品许可证。</li><li>配置身份和身份验证设置</li><li>查看和管理账单信息。</li><li>设置其他管理员和委派角色。</li></ul> **最适合于：**&#x200B;负责监督整个组织的Adobe环境的IT管理员或团队负责人。 |
| 产品管理员 | 产品特定管理 — 控制特定Adobe产品的访问和权限。<br>主要职责：<ul><li>分配和管理特定产品的许可证。</li><li>创建和管理产品配置文件。</li><li>添加或删除已分配产品中的用户。</li></ul>   **最适合于：**&#x200B;管理特定软件(如Marketo Engage或Adobe Creative Cloud)的团队/用户。 |
| 产品配置文件管理员 | 粒度角色管理 — 侧重于管理产品中的用户组和权限。<br>主要职责：<ul><li>创建和管理产品配置文件。</li><li>在配置文件中分配权限和功能访问权限。</li><li>在配置文件中添加或删除用户。</li></ul> **最适合于：**&#x200B;部门主管或团队经理，负责监督具有特殊需求的较小组。 <br>管理员可以根据组织要求合并角色，以获得更大的灵活性。 |

## 适用于Experience Cloud的Admin Console

要管理Experience Cloud应用程序的标识和产品许可证，请导航到[Admin Console](https://adminconsole.adobe.com/enterprise/)。

以下是您在Admin Console中作为管理员快速入门时可能需要的资源：

### 设置资源

| 帮助链接 | 描述 |
| ------- | ------ |
| [设置标识和单点登录](https://helpx.adobe.com/cn/enterprise/using/set-up-identity.html) | **[!UICONTROL Admin Console]** > **[!UICONTROL 设置]** <br>了解如何使用不同的ID类型设置用户的帐户，无论是否使用单点登录(SSO)。 为Adobe软件设置SSO，配置SAML设置，并检查最常见的问题和错误。 |
| [通过目录信任设置组织](https://helpx.adobe.com/enterprise/using/directory-trust.html) | 针对其他组织已声明的域验证您的用户。 有关查找和切换组织的信息，请参阅Experience Cloud中的[组织](organizations.md)。 |
| [身份验证设置（企业）](https://helpx.adobe.com/enterprise/using/authentication-settings.html) | Admin Console支持多种密码保护级别和策略以确保安全性。 您可以指定使用密码保护级别来应用到整个组织中的所有用户。 |
| [隐私和安全联系人](https://helpx.adobe.com/enterprise/using/security-contacts.html) | 保护组织和用户的数据。 如果发生涉及我们软件解决方案的安全事件，我们会将通知发送给相应的合规专员。 企业拥有专门负责数据保护、完整性和其他法规遵从性事务的人员。 因此，此类人员的联系信息对于确保在发生安全事件时及时通知至关重要。 |

### 用户管理

| 帮助链接 | 描述 |
| ------- | ------- |
| [管理多个用户](https://helpx.adobe.com/enterprise/using/bulk-upload-users.html) | **[!UICONTROL Admin Console]** > **[!UICONTROL 用户]** <br>了解如何通过CSV批量上传到Admin Console来管理多个用户。 |
| [身份类型](https://helpx.adobe.com/cn/enterprise/using/identity.html) | 身份类型允许组织对用户的帐户和数据进行不同级别的控制。 您选择的身份模型会影响组织存储和共享资产的方式。 虽然Federated ID和Enterprise ID模型由组织创建和管理，但Adobe ID由个人创建和管理。 |
| [用户同步工具](https://helpx.adobe.com/enterprise/using/user-sync.html) (UST) | Adobe用户同步工具是一个桌面应用程序，用于在组织的身份管理系统（如Active Directory）和Adobe Admin Console之间自动同步用户数据。 借助该工具，管理员可以简化各种Adobe产品中的用户配置、更新和停用操作。 |
| [查看用户详细信息（管理工具）](admin-tool-experience-cloud.md) | 在[!UICONTROL 管理工具]中查看所有Experience Cloud用户和策略的可排序和可过滤列表，以及详细信息。 |

### 报告和日志

| 帮助链接 | 描述 |
| ------- |------- |
| [审核日志](https://helpx.adobe.com/enterprise/using/audit-logs.html) | **[!UICONTROL 分析]** > **[!UICONTROL 日志]** > **[!UICONTROL 审核日志]** <br>跟踪Admin Console中所做的所有更改。 |


## 特定于应用程序的资源

这些链接可帮助您查找特定Experience Cloud应用程序的管理信息。

<!-- | Application | Link to resource|
| ------- | ------- |
|  [!DNL Analytics] <p>Customer Journey Analytics| [Analytics in the Adobe Admin Console overview](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-console/home) <p>[Administration requirements](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/workspace-faq/frequently-asked-questions-analysis-workspace) |
| [!DNL Audience Manager] | [Audience Manager user migration to Admin Console](https://experienceleague.adobe.com/en/docs/audience-manager/user-guide/features/administration/admin-console-migration) |
| [!DNL Campaign] v8 |  [Get started with permissions](https://experienceleague.adobe.com/en/docs/campaign/campaign-v8/admin/permissions/gs-permissions) |
| [!DNL Campaign Standard] to [!DNL Campaign v8] | [User access management from Campaign Standard to Campaign V8](https://experienceleague.adobe.com/en/docs/campaign-web/acs-to-ac/user-management-acs) |
| [!DNL Commerce] | [Configure the Commerce Admin Integration with Adobe ID](https://experienceleague.adobe.com/en/docs/commerce-admin/start/admin/ims/adobe-ims-config) |
| [!DNL Dynamic Media Classic] | [Administration setup](https://experienceleague.adobe.com/en/docs/dynamic-media-classic/using/setup/administration-setup#user_administration) |
| [!DNL Experience Manager as a Cloud Service] |  [Accessing the Admin Console](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/onboarding/journey/admin-console) |
| [!DNL Experience Platform] <p>[!DNL Data Collection] | [Access control UI overview](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/ui/overview) <p>[Permission management for data collection in Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/collection/permissions)|
| [!DNL GenStudio for Performance Marketing] | [Provision Adobe GenStudio for Performance Marketing](https://experienceleague.adobe.com/en/docs/genstudio-for-performance-marketing/user-guide/intro/product-provisioning) |
| [!DNL Journey Optimizer] | [Manage users and roles](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/access-control/permissions) |
| [!DNL Journey Optimizer B2B Edition] | [User management](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/admin/user-management) |
|[!DNL  Journey Orchestration] | [Access management](https://experienceleague.adobe.com/en/docs/journeys/using/starting-with-journeys/access-management) |
| [!DNL Marketo Engage] | [Understanding Marketo Subscription and User Migration to the Adobe Admin Console](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/marketo-with-adobe-identity/subscription-and-user-migration/understanding-marketo-subscription-and-user-migration-to-the-adobe-admin-console) |
| [!DNL Marketo Measure] | [Adobe Admin Console Setup](https://experienceleague.adobe.com/en/docs/marketo-measure/using/configuration-and-setup/getting-started-with-marketo-measure/adobe-admin-console-setup) |
| [!DNL Mix Modeler] | [Access controls](https://experienceleague.adobe.com/en/docs/mix-modeler/using/data-governance/access-controls) |
| [!DNL Pass] | [Get started with Account IQ](https://experienceleague.adobe.com/en/docs/pass/aiq-help/get-started) |
| [!DNL Target] | [Administrator first steps](https://experienceleague.adobe.com/en/docs/target/using/administer/start-target) <p> [User management](https://experienceleague.adobe.com/en/docs/target/using/administer/manage-users/user-management) |
| [!DNL Workfront] | [Manage users in the Adobe Admin Console](https://experienceleague.adobe.com/en/docs/workfront/using/administration-and-setup/add-users/create-manage-users/admin-console) |

 -->

* [Analytics](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-console/home)
* [Customer Journey Analytics](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/workspace-faq/frequently-asked-questions-analysis-workspace)
* [Audience Manager](https://experienceleague.adobe.com/en/docs/audience-manager/user-guide/features/administration/admin-console-migration)
* [Campaign v8](https://experienceleague.adobe.com/zh-hans/docs/campaign/campaign-v8/admin/permissions/gs-permissions)
* [Campaign Standard](https://experienceleague.adobe.com/en/docs/campaign-web/acs-to-ac/user-management-acs)
* [Commerce](https://experienceleague.adobe.com/en/docs/commerce-admin/start/admin/ims/adobe-ims-config)
* [Dynamic Media Classic](https://experienceleague.adobe.com/en/docs/dynamic-media-classic/using/setup/administration-setup#user_administration)
* [Experience Manager as a Cloud Service](https://experienceleague.adobe.com/zh-hans/docs/experience-manager-cloud-service/content/onboarding/journey/admin-console)
* [Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/ui/overview)和[数据收集](https://experienceleague.adobe.com/en/docs/experience-platform/collection/permissions)
* [GenStudio for Performance Marketing](https://experienceleague.adobe.com/en/docs/genstudio-for-performance-marketing/user-guide/intro/product-provisioning)
* [Journey Optimizer](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/access-control/permissions)
* [Journey Optimizer B2B edition](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/admin/user-management)
* [Journey Orchestration](https://experienceleague.adobe.com/en/docs/journeys/using/starting-with-journeys/access-management)
* [Marketo Engage](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/marketo-with-adobe-identity/subscription-and-user-migration/understanding-marketo-subscription-and-user-migration-to-the-adobe-admin-console)
* [Marketo Measure](https://experienceleague.adobe.com/en/docs/marketo-measure/using/configuration-and-setup/getting-started-with-marketo-measure/adobe-admin-console-setup)
* [Mix Modeler](https://experienceleague.adobe.com/en/docs/mix-modeler/using/data-governance/access-controls)
* [Adobe Pass](https://experienceleague.adobe.com/en/docs/pass/aiq-help/get-started)
* [Target](https://experienceleague.adobe.com/en/docs/target/using/administer/start-target)
* [Workfront](https://experienceleague.adobe.com/en/docs/workfront/using/administration-and-setup/add-users/create-manage-users/admin-console)

所有Adobe应用程序的大部分Admin Consol帮助都记录在[企业和团队管理指南](https://helpx.adobe.com/cn/enterprise/admin-guide.html)中。
