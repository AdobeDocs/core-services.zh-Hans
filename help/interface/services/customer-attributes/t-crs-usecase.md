---
description: 了解如何创建 [!DNL Customer Attributes] 数据源并将其上传到Experience Cloud。
solution: Experience Cloud
title: 创建并上传 [!DNL Customer Attributes] 数据Source文件
uuid: 53dca789-9a91-4385-839d-c9d1aa36b9be
feature: Customer Attributes
topic: Administration
role: Admin
level: Experienced
exl-id: 21ed7c35-aac9-46f1-a50c-84e7c075209c
TQID: https://experienceleague.adobe.com/tnqjX4iY7OQx4XW9MjHNg8LaXB1Of6MrtLX-7efyz-E
product_v2: id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
feature_v2: id: fdbb8fc9-ffa3-4b86-88fe-aa4c5a3e1bc6
subfeature_v2: id: b75843fa-0a67-4a44-a6b1-cc627b0481dcid: fef08361-6ac5-460c-93fe-d063e40b6a49
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: d3cdead0-685a-4489-9250-4bb709942f66id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: d57b222077b83d52344a31c8a6b4ccf165843147
workflow-type: tm+mt
source-wordcount: 1118
ht-degree: 47%

---

# 创建和上传客户属性数据

创建客户属性源（`.csv`和`.fin`文件）并上传数据。 您可以在做好准备时激活数据源。 在数据源处于活动状态后，将属性数据共享到[!DNL Analytics]和[!DNL Target]。

**[!DNL Customer Attributes]工作流**

![客户属性工作流程](assets/crs.png)

## 使用[!DNL Customer Attributes]的先决条件 {#prerequisites}

* **组成员资格：**&#x200B;要上传数据，用户必须是[!DNL Customer Attributes]组的成员。 此外，您还必须属于 Adobe Analytics 群组或 Adobe Target 群组。

  要了解您的公司是否具有客户属性的访问权限，您的 [!DNL Experience Cloud] 管理员应当登录到 [Experience Cloud](https://experience.adobe.com)。 导航到&#x200B;**[!UICONTROL Admin Console]** > **[!UICONTROL Products]**。 如果&#x200B;*[!DNL Customer Attributes]*&#x200B;显示为[!UICONTROL product profiles]之一，则表示您已经可以开始。

  添加到[!DNL Customer Attributes]的用户将在Experience Cloud界面的左侧看到[!DNL Customer Attributes]菜单项。

* 客户属性需要使用 **Adobe Target** `at.js`（任何版本）或者 `mbox.js` 版本 58 或更高版本。

  参阅[如何部署 at.js](https://experienceleague.adobe.com/en/docs/target-dev/developer/client-side/overview)。

## 创建数据文件

此数据是 CRM 中的企业客户数据。 数据可能包含产品的订阅者数据，包括成员 ID、授权产品、最常启动产品等。

1. 创建`.csv`文件。

   >[!NOTE]
   >
   >在此过程的后续步骤中，您拖放`.csv`文件以上传该文件。 然而，如果您[通过 FTP 上传](t-upload-attributes-ftp.md#task_591C3B6733424718A62453D2F8ADF73B)，则还需要一个与 `.csv` 文件同名的 `.fin` 文件。

   示例企业客户数据文件：

   ![示例企业客户数据文件](assets/01_crs_usecase.png)

1. 在继续操作之前，请先查看[数据文件要求](crs-data-file.md)中的重要信息，然后再上传文件。
1. [创建客户属性来源并上传数据](t-crs-usecase.md#create-source)，如下所述。

## 创建属性源并上传数据文件

在Experience Cloud的&#x200B;_[!UICONTROL Create Customer Attribute Source]_页面上执行这些步骤。

>[!IMPORTANT]
>
>创建、修改或删除客户属性来源时，大约会有将近一小时的延迟。在此之后，ID 才开始与新的数据源进行同步。 您在 Audience Manager 中必须具有管理权限才能创建或修改客户属性来源。 联系Audience Manager客户关怀团队或咨询以获取管理权限。

1. 要打开[!UICONTROL Customer Attributes]，请单击&#x200B;**[!UICONTROL Apps]** ![菜单](assets/menu-icon.png) > **[!DNL Customer Attributes]**。

   ![客户属性页面](assets/cust-attr.png)

1. 单击 **[!UICONTROL New]**。

   ![步骤结果](assets/new-customer-attribute-source.png)

1. 在[!UICONTROL Create Customer Attribute Source]页面上，配置以下字段：

   * **[!UICONTROL Name:]**&#x200B;数据属性源的易记名称。 对于 [!DNL Adobe Target]，属性名称不能包含空格。 如果传递包含空格的属性，[!DNL Target] 会将其忽略。 其他不受支持的字符包括：`< , >, ', "`。

   * **[!UICONTROL Description:]** （可选）数据属性源的描述。

   * **[!UICONTROL Alias ID:]**&#x200B;表示客户属性数据的来源，如特定的CRM系统。 [!UICONTROL Alias ID]是在您的[!UICONTROL customer attribute Source]代码中使用的唯一ID。 此 ID 应当是唯一的，使用小写字母并且没有空格。 在Experience Cloud中的客户属性源的[!UICONTROL Alias ID]字段中输入的值应与从实施中传入的值（无论是通过Platform Data Collection还是通过Mobile SDK的JavaScript传入）匹配。

     >[!IMPORTANT]
     >
     >删除与别名ID关联的数据源不会使别名ID可用，因为别名ID会保存在多个服务中，并用于在多个服务之间映射配置文件。

     别名ID对应于您在其中设置其他客户ID值的某些区域。 例如：

      * **标记：**&#x200B;别名ID对应于[Experience Cloud ID服务](https://experienceleague.adobe.com/docs/experience-platform/tags/home.html)工具中[!UICONTROL customer Settings]下的&#x200B;*集成代码*&#x200B;值。

      * **访客API：**&#x200B;别名ID对应于可与每个访客关联的其他[客户ID](https://experienceleague.adobe.com/docs/id-service/using/reference/authenticated-state.html)。

        例如，下面的&#x200B;*“crm_id”*：

        ```
        "crm_id":"67312378756723456"
        ```

      * **iOS：**&#x200B;别名ID对应于[visitorSyncIdentifiers:identifiers](https://experienceleague.adobe.com/docs/mobile-services/ios/overview.html?lang=zh-Hans)中的&#x200B;*&quot;idType&quot;*。

        例如：

        `[ADBMobile visitorSyncIdentifiers:@{@<`**`"idType"`**`:@"idValue"}];`

      * **Android™：** 别名 ID 对应于 [syncIdentifiers](https://experienceleague.adobe.com/docs/mobile-services/android/overview.html?lang=zh-Hans) 中的 *&quot;idType&quot;*。

        例如：

        `identifiers.put(`**`"idType"`**`, "idValue");`

        有关别名ID字段和客户ID的数据处理的其他信息，请参阅[利用多个数据源](crs-data-file.md#section_76DEB6001C614F4DB8BCC3E5D05088CB)。

   * **[!UICONTROL Namespace Code:]**&#x200B;在将[IdentityMap](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/identity/overview)用作AEP WebSDK实现的一部分时，使用此值来标识客户属性来源。

1. 单击 **[!UICONTROL Save]**。

## 上传文件 {#upload-customer-attributes}

客户属性记录已创建，您可以通过编辑客户属性来上传文件。

1. 在[!DNL Customer Attributes]页面上，单击属性来源。

1. 在[!UICONTROL Edit Customer Data Source]页面上，单击&#x200B;**[!UICONTROL File Upload]**。

   ![文件上载和架构验证](assets/file-upload-schema-validation.png)

1. 将`.csv`或`.zip`或`.gzip`数据文件拖放到拖放窗口中。

>[!IMPORTANT]
>
>存在特定的数据文件要求。 请参阅[数据文件要求](crs-data-file.md)，以了解更多信息。

上传文件后，表数据将显示在此页面上的[!UICONTROL File Upload]标题下。 您可以验证架构，配置订阅或设置 FTP。

![属性](assets/file_upload_attributes.png)

* **[!UICONTROL Unique customer ID:]**&#x200B;显示您向此属性来源上传了多少个唯一ID。

* **[!UICONTROL Customer-Provided IDs Aliased to Experience Cloud Visitor IDs:]**&#x200B;显示有多少个ID已别名为Experience Cloud访客ID。

* **[!UICONTROL Customer-Provided IDs with High Alias Counts:]**&#x200B;显示具有500个或更多Experience Cloud访客ID别名的客户提供ID的计数。 这些客户提供的 ID 很可能不代表个人，而是表示某种共享登录。 系统会将与这些 ID 关联的属性分发到 500 个最新的 Experience Cloud 访客 ID 别名，直到别名计数达到 10000 个为止。 到那时，系统会使客户提供的ID无效，且不再分发关联的属性。

## 验证架构 {#validate-schema}

验证过程允许您将显示名称和描述映射到已上传的属性（字符串、整数、数字等等）。 您还可以通过更新架构来删除属性。

请参阅[验证架构](validate-schema.md)。

要删除属性，请参阅[（可选）更新架构（删除属性）](t-crs-usecase.md)。

## （可选）更新架构（删除属性）

如何删除和替换架构中的属性。

1. 在[!UICONTROL Edit Customer Attribute Source]页面上，删除&#x200B;**[!UICONTROL Target]**&#x200B;或&#x200B;**[!UICONTROL Analytics]**&#x200B;订阅（在&#x200B;**[!UICONTROL Configure Subscriptions]**&#x200B;下）。

1. [上传具有更新字段的新数据文件](t-crs-usecase.md)。

## 配置订阅和激活属性源

配置订阅可以设置Experience Cloud和应用程序之间的数据流。 激活属性来源后，数据便可流向订阅的应用程序。 您上传的客户记录与来自您网站或应用程序的传入 ID 信号相匹配。

请参阅[配置订阅并激活数据源](subscription.md)。

## 在Adobe Analytics中使用[!DNL Customer Attributes]数据

利用 Adobe Analytics 等应用程序中现在提供的数据，您可以报告数据、分析数据并在营销活动中采取适当措施。

以下示例显示了一个基于上传属性的 [!DNL Analytics] 区段。 此区段显示最常启动产品为 Photoshop 的 [!DNL Photoshop Lightroom] 订阅者。

![基于已上传属性的 Analytics 区段](assets/08_crs_usecase.png)

在将区段发布到Experience Cloud时，它将在Experience Cloud受众和Audience Manager中变得可用。

## 在Adobe Target中使用[!DNL Customer Attributes]数据

在[!DNL Target]中，您可以在创建受众时从[!UICONTROL Visitor Profile]部分中选择客户属性。 列表中的所有客户属性都有前缀`crs.`。 可根据需要，将这些属性与其他数据属性结合使用以构建受众。

![在 Adobe Target 中使用客户属性](assets/crs-add-attribute-target.png)

请参阅[!DNL Target]帮助中的[创建受众](https://experienceleague.adobe.com/docs/target/using/audiences/create-audiences/audiences.html?lang=zh-Hans)。
