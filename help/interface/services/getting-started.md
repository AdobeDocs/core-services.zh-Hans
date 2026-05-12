---
description: 实现 Adobe Analytics 和 Adobe Target 应用程序的现代化，以提供跨应用程序服务。 了解如何开始使用CX企业服务。
solution: Experience Cloud
title: Experience Cloud服务入门
index: true
feature: Central Interface Components
topic: Administration
role: Admin
level: Experienced
exl-id: 48e79e23-b339-4143-b3b1-969c370efeff
TQID: https://experienceleague.adobe.com/5SyRdqyQkymJJygKeQ9FXIYoVe70br51DY2VKmqSC0E
product_v2: id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
feature_v2: id: dab36b01-8bfa-48f3-8392-626455a058e6id: fdbb8fc9-ffa3-4b86-88fe-aa4c5a3e1bc6
subfeature_v2: id: b75843fa-0a67-4a44-a6b1-cc627b0481dcid: bdea9bc8-5600-45db-b85e-d74bb59dfcffid: d27b1945-f442-4607-91bd-537a0b16e687id: eb7e29b9-c5e9-4ed0-8e4b-6465dabb3cb1id: ecb4a972-6786-444c-a014-abc528b9407aid: fef08361-6ac5-460c-93fe-d063e40b6a49
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: c2be0313-b3ae-45e0-b454-d20bf54b23f2id: d3cdead0-685a-4489-9250-4bb709942f66id: e0eb8757-182f-49f3-94a4-1587d16f5094id: eddd9b14-83bd-4ff4-9072-54a4a484abb7id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 50012e2564e88e1a6e16578e3331136c7df0cb21
workflow-type: tm+mt
source-wordcount: 2150
ht-degree: 42%

---

# 开始使用CX Enterprise

如果您最近使用[Experience Platform标记](https://experienceleague.adobe.com/en/docs/experience-platform/tags/home)实施了CX Enterprise，则已经为[客户属性](../services/overview.md)和CX Enterprise [受众](../services/audiences/overview.md)进行了设置。 您还可以在[Admin Console](../administration/admin-console.md)中管理用户和产品。

现有客户可以使其应用程序实施实现现代化并实施CX Enterprise。 这样，您就可以在Adobe Analytics、Audience Manager和Adobe Target中使用客户属性和受众功能。

## 以管理员身份登录 {#admin-sign-in}

在成为管理员后，您可以登录到 [experience.Adobe.com](https://experience.adobe.com).

CX Enterprise菜单导航中提供了&#x200B;**[!UICONTROL Admin Console]**&#x200B;链接，用于管理用户和产品许可证。

### 可选：链接现有用户帐户 {#link-accounts}

您的用户很有可能已经是应用程序组的成员，例如先前在[!UICONTROL Analytics] > [!UICONTROL Admin Tools]中管理的Analytics组。

将这些组映射到CX企业组时，这些用户必须手动将其应用程序帐户凭据关联到其Adobe ID。

查看CX Enterprise中的[关联帐户](https://experienceleague.adobe.com/en/docs/core-services/interface/administration/organizations)

>[!NOTE]
>
>在映射企业群组和应用程序群组后，将会自动关联新用户。 （将自动创建解决方案凭据，并将凭据关联到其 Adobe ID。）

以下各节介绍如何使实施符合现代化要求。 使实施实现现代化可以在CX Enterprise中启用核心服务。

## 以用户身份登录 {#user-sign-in}

要登录到CX Enterprise ，您的用户必须：

* 拥有 Adobe ID（或您公司的 Enterprise ID）。
* 登录到 [experience.Adobe.com](https://experience.adobe.com)。
* 属于映射到企业群组的应用程序群组。
* 如有必要，请将其应用程序帐户关联到 Adobe ID（如下所述）。

## CX企业版的Adobe Analytics和Adobe Target要求 {#experience-cloud-requirements}

使用CX Enterprise的[!DNL Analytics]和[!DNL Adobe Target]要求：

1. 确保您拥有适当的 Adobe Analytics 或 Adobe Target SKU。

   * **Adobe Analytics：** Standard 或 Premium（不是旧版 [!DNL SiteCatalyst] SKU）。
   * **Adobe Target：** Standard 或 Premium。

     >[!NOTE]
     >
     >对于 [!DNL Target]，请从 `mbox.js` 迁移到 at.js。 请参阅[从at.js 1. x到at.js 2. x](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/upgrading-from-atjs-1x-to-atjs-20.html)。

1. 在[!UICONTROL Admin Console]中[管理用户和产品](../administration/admin-console.md)。

**相关：** [Analytics和Target — 同步客户ID](#sync-ids)（在此页面上）

## 实施 [!UICONTROL CX Enterprise ID Service]

[!UICONTROL CX Enterprise ID Service]为跨应用程序集成提供了一个通用ID。 它提供了跨域访客标识功能，并为基于通过[!DNL Customer Attributes]上传的CRM数据进行跨设备/浏览器定位和个性化提供了一种途径。

启用CX Enterprise核心服务的最简单方法是，通过[!UICONTROL Experience Platform Launch]中的[CX Enterprise ID Service扩展](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/adobe/id-service/overview.html)，为Analytics和Adobe Target自动激活核心服务。

>[!NOTE]
>
>有关完整的CX Enterprise ID服务帮助（以前称为访客ID），请参阅[CX Enterprise Identity Service概述](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html#intro)。


**未使用[!UICONTROL Experience Platform tags]？**

如果您没有使用[!UICONTROL Experience Platform tags]，请通过JavaScript部署(`VisitorAPI.js`)手动实施ID服务，如下所示：

| 任务 | 描述 |
| --- | --- |
| [为Analytics实施CX Enterprise ID服务](https://experienceleague.adobe.com/en/docs/analytics/implementation/id/overview) | Adobe 还建议设置其他[客户 ID](https://experienceleague.adobe.com/en/docs/id-service/using/reference/authenticated-state)。 这些ID与每个访客相关联，并可以启用CX Enterprise中当前和未来的功能。 |
| 将现有的 `s_code` 更新到 H.27.3 或更高版本，或将现有的 `AppMeasurement.js` 更新到 1.4 或更高版本。 | 这些文件可通过在 Analytics 管理工具的[代码管理器](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/code-manager-admin.html)中下载获得。 （如果您需要了解有关 `AppMeasurement.js` 的更多信息，请参阅 [JavaScript 实施](https://experienceleague.adobe.com/en/docs/analytics/implementation/js/overview#js)指南。） |

### Analytics和Adobe Target — 同步客户ID {#sync-ids}

在设置CX Enterprise ID服务时，Adobe建议您针对Analytics和[!DNL Target]考虑将您的[客户ID](https://experienceleague.adobe.com/docs/id-service/using/reference/authenticated-state.html)与CX Enterprise同步。

在 Adobe Target 中，`mbox3rdpartyid` 必须获取客户 ID 并将其发送给 [!DNL Target]。 （请参阅 [!DNL Target] 中的[使用客户属性](https://experienceleague.adobe.com/docs/target/using/audiences/visitor-profiles/working-with-customer-attributes.html?lang=zh-Hans)。）

当访客在您的网站上进行身份验证或以其他方式标识自己时，您的实施必须向页面或应用程序公开访客的 CRM 客户 ID。 然后，您可以使用相应的函数调用将您的客户ID同步到CX Enterprise。 此同步会将访客的CRM客户ID存储在CX Enterprise中，并激活该客户的属性以在CX Enterprise中使用。

例如，假设 Bob 在您的 CRM 系统中具有客户 ID `52mc210tr42`。 当 Bob 在您的网站上进行身份验证时，您必须在该页面上透露此 ID，并使用此 ID 以下面两种方式之一进行同步：

* 使用访客 ID 服务调用 `visitor.setCustomerIDs({"crm_id":"52mc210tr42"})`。 或,
* 在 prop 或 eVar 中填充 *`Customer ID (52mc210tr42)`*。

在已知客户 ID 的情况下，必须在每次 [!DNL Analytics] 服务器调用中进行设置。

#### Analytics：将客户 ID 与 Data Warehouse 回填方法同步

当客户属性首次可用时，一些客户尚未实施CX Enterprise ID服务，因而不能方便地使用客户属性。 为了帮助缓解这个问题，Adobe 创建了一种使用 Adobe Analytics Data Warehouse 来回填 ID 同步的方法。 此功能称为 Data Warehouse 回填。 现在通常没有必要对 Data Warehouse 进行回填，因此从 2022 年 10 月起不再可用。

### Mobile SDK

有关如何在[Android](https://experienceleague.adobe.com/docs/mobile-services/android/overview.html?lang=zh-Hans)和[Enterprise ID](https://experienceleague.adobe.com/docs/mobile-services/ios/overview.html?lang=zh-Hans)移动应用程序中设置其他客户ID的语法示例，请参阅&#x200B;*CXiOS服务™1}部分。*

### 启用历史数据的属性

客户属性数据在访客登录后可用。 如果您尚未实施ID服务，并且以前一直在prop或eVar中跟踪客户ID，则可以请求一个流程，以将历史登录发送到CX Enterprise。 凭借此流程，您可以立即开始使用客户属性。

请联系支持以启用历史数据。

## 将报表包映射到CX Enterprise组织

>[!NOTE]
>
>报表包映射功能已于 2020 年 11 月被弃用。 如有任何问题，请联系客户支持。

CX Enterprise服务（如CX Enterprise ID服务）与CX Enterprise组织相关联，而不是与单个Analytics报表包关联。 为确保这些服务能够正确运行，必须将每个Analytics报表包映射到CX Enterprise组织。

## 更新 Analytics AppMeasurement 代码

如果您使用的是第一方Cookie，请参阅[CNAME和CX Enterprise ID服务](https://experienceleague.adobe.com/docs/id-service/using/reference/analytics-reference/cname.html)以了解有关数据收集CNAME和跨域跟踪的信息。

建议您更新包括访客 API 在内的 JavaScript 库，以使您的 Analytics 实施现代化。 一个简单方法是在 Experience Platform 数据收集中添加 [Adobe Analytics 扩展。](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/adobe/analytics/overview.html)

## 更新 Adobe Target 实施

* 建议您在[!UICONTROL Experience Platform]标记中添加[Adobe Target扩展](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/adobe/target-v2/overview.html)，以便自动检索库。 您还可以使用[!UICONTROL Experience Platform]标记为Adobe Target（和其他应用程序）设置[CX Enterprise ID服务扩展](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/adobe/id-service/overview.html)。 需要[!UICONTROL CX Enterprise ID Service]更新&#x200B;**才能Adobe Target使用People服务**。
* 如果您没有使用[!UICONTROL Experience Platform]标记，请手动[更新mbox库](https://experienceleague.adobe.com/docs/target/using/implement-target/client-side/implement-target-for-client-side-web.html)。
* 请求访问权限，以使用 Adobe Analytics 作为 [!DNL Adobe Target] 的报表源。 在处理期间，[!DNL Target] 和 [!DNL Analytics] 数据将组合在同一服务器调用中，这样两个应用程序的访客就可以连接在一起。 请参阅 [Analytics for Target 实施](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html)。

  >[!IMPORTANT]
  >
  >已针对客户属性等核心服务配置了所有 Analytics 客户。 如果您不是 Analytics 客户，请联系客户关怀团队以请求进行配置。

## 验证实施

请使用以下过程以确保在您的网站上正确实施CX Enterprise ID服务。

1. 清除网站的Cookie，以便您能够看到对CX Enterprise ID服务的请求（请求在首次访问时发生，随后每周为每位访客发生一次）。
1. 使用一个数据包分析程序或 Web 浏览器调试程序中的网络面板，查找到 [!DNL dpm.demdex.net] 的请求。
1. 验证响应中是否包含 `d_mid` 和一个值，例如：`_setMarketingCloudFields({"d_mid":"4235...`
1. 验证Analytics请求是否包含`mid`参数(CX Enterprise ID)。 在宽限期内（如果启用），您还应看到 `aid` 参数（Analytics 访客 ID）。

包含CX Enterprise ID的预期响应：

![预期响应包含CX Enterprise ID](../assets/mac_id_response.png)

包含CX Enterprise ID（也称为`mid`或&#x200B;_访客ID_）的Analytics图像请求：

![包含CX Enterprise ID的Analytics图像请求](../assets/mid.png)

mbox请求中的CX Enterprise ID：

mbox请求中的![CX Enterprise ID](../assets/mbox_request.png)

### 什么是宽限期？

在您部署CX Enterprise ID服务后，新的访客将不再从您的数据收集服务器中接收Analytics CX Enterprise ID。 如果您网站的某些部分尚未实施ID服务，那么当访客浏览这些部分时，将无法识别CX Enterprise ID，与此同时，分配给访客的会是一个旧版Analytics访客ID。 这可能会导致潜在的问题，包括重复访问和错误归因。

例如，如果网站的支持部分是在单独的 CMS 中管理的，则此部分可能有不同的 Analytics JavaScript 文件。 如果您在将ID服务部署到支持网站之前，在主要网站上部署了CX Enterprise ID，则新访客在访问支持部分时会收到一个旧版Analytics ID。 跨两个网站区域的访问报告为不同的访问。

在使用多个JavaScript文件或其他技术（如Flash）的网站上部署CX Enterprise ID服务时，可能会导致协调问题。 出现这些问题是因为您必须同时在站点的所有部分上启用CX Enterprise ID服务。 通过配置一个宽限期，新的访客可以继续从ID服务中接收Analytics访客ID。 对于网站中没有升级为使用访客ID服务的部分，可以始终如一地识别访客。

## 管理用户和产品

启动并运行后，导航至 [Admin Console](https://adminconsole.adobe.com/)，您可以在其中管理用户和产品轮廓。

![访问 Admin Console](../assets/menu-administration-shell.png)

### 客户属性

添加到[!DNL Customer Attributes]组的用户可以在CX Enterprise的左侧看到[!DNL Customer Attributes]菜单项。

## 开始共享属性和受众数据

充分利用以下功能。

### [!UICONTROL Customer Attributes]

如果您在客户关系管理(CRM)数据库中捕获到企业客户数据，则可以将该数据上传到CX Enterprise中的客户属性数据源。 上传后，即可在 [!DNL Adobe Analytics] 和 [!DNL Adobe Target] 中利用这些数据。

有关详细信息，请参阅[客户属性](https://experienceleague.adobe.com/en/docs/core-services/interface/services/customer-attributes/attributes)。

### [!UICONTROL People] > [!UICONTROL Audience Library]

CX Enterprise [!UICONTROL Audiences]是一个界面，您可以从这里创建受众，合并现有受众以创建复合受众，以及查看所有共享受众。

有关详细信息，请参阅[受众](https://experienceleague.adobe.com/en/docs/core-services/interface/services/audiences/overview)。

## 数据存储和隐私披露

如果在 Adobe [!DNL CX Enterprise] 中使用实时受众分析和其他核心服务，那么运用这些服务时，可能会影响数据存储到的数据中心（和国家/地区）。 具体来讲，因为[!DNL CX Enterprise]使用Audience Manager，所以在[!UICONTROL People]服务中使用的数据必须存储在位于美国的Audience Manager服务器上。

使用通过[!UICONTROL People]服务提供的服务时，从其他Adobe产品向受众管理发送的数据类型包括：

* [!DNL Analytics] 键/值对（prop、eVar、list var 等等）。 默认情况下，日志行包含 IP 地址，其中包含 IP 的最后一个八位字节（假定 IP 地址没有被 Adobe [!DNL Analytics] 中的 IP 模糊设置所修改）。
* 根据 Audience Manager 中设置的规则，受众符合资格的特征和区段。
* （可选）您的一个或多个 ID。 根据 ID 服务的实施，您可能还会发送一个或多个 ID，例如 CRM ID 或哈希电子邮件地址。 如果此数据被发送到 Adobe [!DNL Analytics]，则会转给 Adobe 受众管理。 Adobe 不建议将个人数据提交给 Adobe [!DNL Analytics]。 而是使用单向哈希对数据进行掩饰，然后再发送给 Adobe。
* 来自 [!DNL Analytics] 且通过后端区段共享功能获得的区段。
* 如果未阻止第三方 Cookie，则设置 demdex.net Cookie。 `AMCV_###@AdobeOrg`第一方Cookie始终通过CX Enterprise ID服务进行设置。

所有这些数据元素都将以日志文件的形式传送到 Adobe Audience Manager。 Audience Manager 将在美国境内的服务器上处理并存储这些数据。 Audience Manager 不提供在美国境外的服务器上存储或处理此数据的选项。
