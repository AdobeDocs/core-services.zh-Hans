---
description: 了解 Adobe Experience Cloud 中的可用应用程序集成。
solution: Experience Cloud
title: Experience Cloud 集成
uuid: a9893c6b-bccc-4fb5-b724-724644c7def5
feature: Admin Console
topic: Administration
role: Admin
level: Experienced
exl-id: 7f8fa610-32f0-4b18-8054-3ba05436a10e
source-git-commit: a4e0461791cd676365857c2dd4ef28c0e40c3430
workflow-type: tm+mt
source-wordcount: '903'
ht-degree: 74%

---

# Experience Cloud 集成概述

本页介绍了几种开始集成Experience Cloud应用程序的方法。 有关详细信息，请浏览Experience League上的[集成视频教程](https://experienceleague.adobe.com/docs/experience-platform/tags/home.html?lang=zh-Hans)库。

## 为 Platform 服务启用您的 Experience Cloud 应用程序 {#section_A3D024994DA3492F8435CFCC4EF035C2}

介绍如何执行操作：

* 在Experience Cloud中配置您的公司。
* 让您成为管理员。
* [实施 Experience Cloud ID 服务](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=zh-Hans)。
* 通过[!UICONTROL 平台数据收集]使您的[!DNL Analytics]和[!DNL Target]实现现代化。
* 开始使用[[!DNL Customer Attributes]](../services/customer-attributes/attributes.md)和[[!DNL Audience Library]](../services/audiences/overview.md)等Experience Cloud服务。

解决方案或服务：

* [[!DNL Experience Platform Data Collection]](https://experienceleague.adobe.com/docs/experience-platform.html?lang=zh-Hans)
* [[!DNL Analytics]](https://experienceleague.adobe.com/docs/analytics.html?lang=zh-Hans)
* [[!DNL Target]](https://experienceleague.adobe.com/docs/target.html?lang=zh-Hans)
* [Experience Cloud ID 服务](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=zh-Hans)

## Experience Cloud ID 服务 {#section_6ECCCFA2D84D4D4F88C879C799CA9D78}

ID服务提供一个通用、永久性的ID，后者在Experience Cloud的所有应用程序中标识您的访客。 它可取代 Analytics、Audience Manager、Adobe Target、视频检测信号和其他 Experience Cloud 应用程序和产品等服务的 ID 生成代码。

请参阅 [Experience Cloud ID 服务](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=zh-Hans)。

**适用的应用程序或服务**

* [Adobe Analytics](https://experienceleague.adobe.com/docs/id-service/using/implementation/setup-analytics.html?lang=zh-Hans)
* [Adobe Target](https://experienceleague.adobe.com/docs/id-service/using/implementation/setup-target.html?lang=zh-Hans)

## 受众 {#section_5F60D7B0833348B9A1D74663AADCB42C}

帮助：[受众](/help/interface/services/audiences/overview.md)

在Experience Cloud[!UICONTROL 受众库]中创建和管理受众。 受众可从各种来源创建或派生，如：

* 在 [!DNL Experience Cloud] 中创建新受众。
* 从 [!DNL Analytics] 发布到 [!DNL Experience Cloud] 的区段。
* 从 [!DNL Audience Manager]。

**适用的解决方案或服务**

* [Adobe Target 中的活动](https://experienceleague.adobe.com/docs/target/using/activities/activities.html?lang=zh-Hans)
* Audience Manager 中的[分段](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/audience-analytics-workflow/aam-analytics-segments.html?lang=zh-Hans)
* [Advertising Cloud](https://enterprise.efrontier.com/CMDashboard/?ticket=JrciD7q2bF1y2mDWFHmEyibbOnNwb2JBRF7z6tKAOIWkBimlPxCUaZyJnPLqsfdqsf3fpxWoxGasvatKA8S6-h4tlDvxQcm8Gc10dSF9q_E%3D&amp;ticket=JrciD7q2bF1y2mDWFHmEyibmxtHqnZFSOMml-n993zOBc-ovZGNZkX5vgePWqKNMoMmPSqf9PkzFeYF4UN6GqSXDVNDvwgnvv9KT8PvVxk8%3D) （需要登录）

## 客户属性 {#section_6A9EA6847F654F129381869E5016626C}

帮助：[客户属性](/help/interface/services/customer-attributes/attributes.md)

如果您在客户关系管理 (CRM) 数据库中捕获到企业客户数据，则可以将该数据上传到 Experience Cloud 中的客户属性数据源。上传后，即可在 [!DNL Adobe Analytics] 和 [!DNL Adobe Target] 中利用这些数据。

**适用的解决方案或服务**

* Adobe Analytics：客户属性报表
* Adobe Target：配置 Adobe Target 的客户属性[订阅](/help/interface/services/customer-attributes/subscription.md)

## Experience Cloud 资产 {#section_92BC5DFDB0E0499CB0DD34B85E06F79A}

帮助：[与 Creative Cloud 共享 Experience Cloud 文件夹](/help/interface/services/assets/creative-cloud.md)

在 Experience Cloud 和 Creative Cloud 之间共享文件夹和资产。在Experience Cloud应用程序(如Adobe Target)中进行协作、对共享资源添加批注和使用它们。

**适用的应用程序或服务**

* Adobe Experience Cloud
* Adobe Creative Cloud
* Adobe Target

## Analytics - Analytics 中的 AEM Assets 报表 {#section_0A16AE14F128470AA02EFC6457BDCE75}

帮助：[Analytics 中的 AEM Assets 报表](https://experienceleague.adobe.com/docs/analytics/integration/aem-assets-reporting.html?lang=zh-Hans)

使 Analytics 能够从 AEM 资源分析收集投放资源的展示次数和点击次数。

**适用的应用程序或服务**

* [!DNL Analytics]
* [!DNL Experience Manager]

## Audience Manager 集成 {#section_8FEFE1746E26416EB7E73095BBAD5345}

[Audience Manager](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/implementation-and-integration.html?lang=zh-Hans)

在 Audience Manager 中处理来自 Experience Cloud 应用程序或其他外部系统的数据。

**适用的应用程序或服务**

* [Analytics 服务器端转发](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/server-side-forwarding/ssf.html?lang=zh-Hans)
* [将 Audience Manager 发送到 Analytics](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/destinations/experience-cloud-destinations/create-analytics-destination.html?lang=zh-Hans)
* [Adobe Target 数据集成](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/integration-other-applications/aam-target-integration.html?lang=zh-Hans)

## Adobe Target {#section_739716AB6022424CBC38724CDED10701}

帮助： [将Adobe Target与Experience Cloud集成](/help/interface/services/audiences/overview.md)

将 Adobe Target 与 Adobe Analytics 及其他 Experience Cloud 应用程序集成，以便能够在两个应用程序中使用相同的数据、受众、属性和量度。

**适用的应用程序或服务**

* 客户属性：配置 Adobe Target 的客户属性[订阅](/help/interface/services/customer-attributes/subscription.md)
* Experience Cloud 受众：[Experience Cloud Audience Library](/help/interface/services/audiences/overview.md)
* Analytics：[将 Adobe Analytics 作为 Adobe Target 报表源](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html?lang=zh-Hans)
* Audience Manager：[Adobe Target 与 Adobe Audience Manager 的数据集成](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/integration-other-solutions/aam-target-integration.html?lang=zh-Hans)
* Campaign：[将 Adobe Target 与 Campaign 集成](https://experienceleague.adobe.com/docs/target/using/integrate/campaign-and-target.html?lang=zh-Hans)

## Experience Manager 集成 {#section_32FB010EF8B4429FBC63C8DC2A9BE98F}

* 视频教程： [Experience Manager集成](https://experienceleague.adobe.com/docs/integrations-learn/experience-cloud/integrations-between-applications/overview.html?lang=zh-Hans)

* 产品文档： [Experience Manager文档](https://experienceleague.adobe.com/docs/experience-manager-cloud-service.html?lang=zh-Hans)

## Experience Manager - Assets {#section_CB865F8EFE4C4147BF8E2E4B66B5A318}

帮助：[配置 AEM Assets 与 Experience Cloud 和 Creative Cloud 的集成](https://experienceleague.adobe.com/docs/?lang=zh-Hans)

将 Adobe Experience Manager (AEM) Assets 中的资源与 Adobe Creative Cloud 同步，反之亦然。您还可以将资源与 Experience Cloud 同步，反之亦然。您可以通过 Experience Cloud 设置此同步。

**适用的应用程序或服务**

* AEM
* Creative Cloud
* [Experience Cloud](https://experienceleague.adobe.com/docs/?lang=zh-Hans)

## [!DNL Adobe Advertising] {#section_9B1935F8BBC147C89C6DB68A35CB1BAB}

* 帮助（需要登录）：[与 Adobe Experience Cloud 解决方案和服务的集成](https://enterprise.efrontier.com/CMDashboard?ticket=JrciD7q2bF1y2mDWFHmEyhyMKZp71ZLeaANvF-RcNMF7oNuZNABh76cKJLNlJJeJ1hQ5vAW1AO1t1DW8tZWM3lYZ8TSh96YAQISUdtHCCgA%3D&amp;ticket=JrciD7q2bF1y2mDWFHmEyibbOnNwb2JBRF7z6tKAOIWkBimlPxCUaZyJnPLqsfdqsf3fpxWoxGasvatKA8S6-h4tlDvxQcm8Gc10dSF9q_E%3D)

* Experience League上的[Adobe Advertising文档](https://experienceleague.adobe.com/docs/advertising.html?lang=zh-Hans)

**适用的应用程序或服务**

**Analytics：**&#x200B;可每天将网站参与和转化数据发送到 [!DNL Adobe Advertising]，从中可将这些数据用于广告优化和报表。此外，[!DNL Advertising] 还可每天将搜索引擎和社交网络流量数据发送到 Analytics，从中可将这些数据用于 Reports &amp; Analytics、Report Builder 和临时分析功能中的报表。

**标记：**&#x200B;您可以使用[Experience Platform标记创建基于Advertising像素的转化跟踪标记](https://experienceleague.adobe.com/docs/experience-platform/tags/home.html?lang=zh-Hans)以及第三方跟踪标记，以用于您的搜索、社交和显示广告登录页。 （还可直接在 [!DNL Advertising] 内创建 [!DNL Advertising] 标记）

**Experience Cloud 受众：**（需要管理显示的广告商）可适用任何 [Adobe Experience Cloud 受众](../services/audiences/overview.md)作为显示广告的目标。您可以自动使用在Experience Cloud中创建的受众和Analytics中已发布到Experience Cloud的受众。 将[!DNL Adobe Advertising]帐户配置为允许使用Audience Manager中的受众时，您也可以使用该受众。

有关访问 Adobe Experience Cloud 以及个人资料和受众以及有关 [!DNL Adobe Advertising] 与 Adobe Experience Cloud 受众之间的初始设置的详细信息，请与您的客户经理联系。**注意：**&#x200B;如果您还使用 Adobe Target，则您发布到 Adobe Experience Cloud 的任何受众也可用于 Adobe Target 中的活动。

**Experience Cloud 资产：**（具有显示管理需求的广告商）您可以通过新的显示测试版视图，将任何 Adobe Experience Cloud 资产用作显示广告的创意。您必须是[登录才能通过Adobe Experience Cloud](https://enterprise.efrontier.com/CMDashboard)Adobe Advertising访问您的Adobe Experience Cloud资源。 有关访问 Adobe Experience Cloud 的信息，请与您的客户经理联系。

**Experience Cloud 通知：**&#x200B;通过每页顶部的通知链接，您可以查看基于搜索测试版警报模板生成的所有警报。您还可以获取有关 Experience Cloud 系统更新、帖子、提及次数和共享资源的通知。您必须是[登录才能通过Adobe Experience Cloud](https://enterprise.efrontier.com/CMDashboard)Adobe Advertising您的通知。 有关访问 Adobe Experience Cloud 的信息，请与您的客户经理联系。
