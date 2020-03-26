---
description: Experience Cloud 中与管理员有关的常见问题及解答。
keywords: core services
seo-description: Experience Cloud 中与管理员有关的常见问题及解答。
seo-title: 常见问题解答
solution: Experience Cloud
title: 常见问题解答
uuid: 3ed0b4eb-690f-4c14-a31c-0cc1118fb3b4
translation-type: tm+mt
source-git-commit: f7ec8bf6087a18be41c9efbf05f60e6cfd24e566

---


# 常见问题解答

Experience Cloud 中与管理员有关的常见问题及解答。

**如何知道是否已为核心服务启用我的解决方案？**

如果尚未为核心服务配置实施，请参阅[为核心服务启用解决方案](../core-services/core-services.md#concept_07ED1D5C64234E77976E6D572E78FB9C)，其中介绍了以下操作说明：

1. [加入 Experience Cloud 并成为管理员](../core-services/core-services.md#section_2423F0BD3DF642658103310EE5EA6154)
1. [使用动态标签管理器](../core-services/core-services.md#section_3C9F6DF37C654D939625BB4D485E4354) (或新的Experience Platform Launch [](https://docs.adobe.com/content/help/en/launch/using/intro/get-started/quick-start.html))实施Experience Cloud ID服务
1. [将报表包映射到 Experience Cloud 组织](../core-services/core-services.md#concept_apg_zq2_rw)
1. [（仅限Analytics）使您的Analytics AppMeasurement代码现代化](../core-services/core-services.md#section_1798D9D0F05C47E29816AC4EEB9A0913)
1. [(仅限Adobe目标)使您的Adobe目标实施现代化](../core-services/core-services.md#section_C2F4493C7A36406DAE2266B429A4BD24)
1. [验证核心服务实施](../core-services/core-services.md#section_E641782A0F4F44AF8C9C91216BE330D5)
1. [管理用户和产品](../core-services/core-services.md#section_B6E95F4E0E12483CB9DA99CBC0C5A4AF)
1. [开始使用核心服务](../core-services/core-services.md#section_960C06093623462E8EA247B3E97274A1)

要获得更多帮助，请 [与Adobe支持部门联系](https://helpx.adobe.com/marketing-cloud/contact-support.html)。

**Adobe 会对我的公司收取 Experience Cloud 的访问费用吗？**

否。Experience Cloud不收取任何额外费用。 但是，某些核心服务可能会产生额外成本。

**为什么我的公司需要通过 Experience Cloud 界面登录？**

Experience Cloud界面提供的功能为您的业务增加了新的价值。 它还将成为今后访问解决方案的标准途径，最终取代其他单独的解决方案登录流程。 通过Experience Cloud登录后将更顺畅地过渡。

**如何消除有关迁移我的公司的疑虑？**

[联系Adobe支持](https://helpx.adobe.com/marketing-cloud/contact-support.html)。

**什么是供&#x200B;_应？_**

Experience Cloud 中的配置表示：

* 您的用户可以开始登录到 [!DNL Experience Cloud] 并关联解决方案。
* 他们可以开始使用Experience Cloud提供的功能，如“人员”。
* 您可以准备好退出特定于解决方案的登录过程。
* 您可以保留对解决方案的访问控制。

**如何管理用户和产品配置文件？**

* 有关帮助， [请参阅Admin Console用户指南](https://helpx.adobe.com/enterprise/administering/user-guide.html) 。

* 用户权限和产品管理在 [Adobe Admin Console](https://adminconsole.adobe.com/enterprise)（产品链接）中执行。

* **重要说明：** 分析管理员，请参 [阅管理控制台中的管理分析用户](https://docs.adobe.com/content/help/en/analytics/admin/user-product-management/user-management/migrate-users/c-migration-tool.html) ，了解如何将用户ID从Analytics管理工具迁移到管理控制台。

**如果有人无法登录到 Experience Cloud，我该怎么做？**

Admin Console管理员可以授予用户访问权限。 用户会收到带有登录说明的电子邮件。

You might need to [Contact Adobe Support](https://helpx.adobe.com/marketing-cloud/contact-support.html) to verify that your company has been fully provisioned.

**用户可在何处管理帐户关联？**

有些用户可能需要将其解决方案 (Analytics) 帐户关联到 Adobe ID 或 Enterprise ID。

See [Link a solution account to an Adobe ID](../admin-getting-started/organizations.md#task_FD389E78640848919E247AC5E95B8369).

**如何管理用户帐户配置文件和组织？**

请参阅[管理用户帐户](../admin-getting-started/organizations.md#topic_C31CB834F109465A82ED57FF0563B3F1)。

**什么是组织？**

** 组织是一个实体，它允许管理员配置群组和用户，并控制 Experience Cloud 中的单点登录。组织的作用类似于一个衔接所有 Experience Cloud 产品和解决方案的登录公司。大多数情况下，组织是您的公司名称。 但是，公司可以有许多组织。

**我可以在哪里找到我的 IMS 组织 ID？**

请参阅[查找组织 ID](organizations.md)。

组织 ID 显示在 Experience Cloud 登录页面和 [Admin Console 登录页面](https://adminconsole.adobe.com)中。

Alternatively, administrators can log into the Admin console (Navigate to [https://adminconsole.adobe.com](https://adminconsole.adobe.com#)) for a specific organization, and you will be able to see your IMS org ID in the URL.

例如，在以下 URL 中：

`https://adminconsole.adobe.com/C538193582390300A495CC9@AdobeOrg/overview`

ID 为：

`C538193582390300A495CC9@AdobeOrg`

**如果我的一位用户离开了我的公司怎么办？**

应将他们的访问权限从解决方案中删除。他们将无法通过Experience Cloud或直接登录访问产品。 您还应在Experience Cloud级别删除这些组件。

**什么是 Adobe ID？**

请参阅 [标识类型](https://helpx.adobe.com/enterprise/help/identity.html)。

**我可以为我的用户关联解决方案帐户吗？**

否。用户必须将自己的解决方案与其用户名和密码相关联。

**为什么我的公司没有 Social 但是我却能看到？**

Adobe Social是一款可与Analytics一起销售的产品。 因此，如果您拥有Analytics，您将看到此解决方案，但除非您已购买它，否则您将无权访问它。