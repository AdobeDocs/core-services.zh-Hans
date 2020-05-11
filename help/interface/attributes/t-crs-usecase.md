---
description: 创建客户属性来源并上传数据。
keywords: Customer Attributes;core services
seo-description: 创建客户属性来源并上传数据。
seo-title: 创建客户属性来源并上传数据文件
solution: Experience Cloud
title: 创建客户属性来源并上传数据文件
uuid: 53dca789-9a91-4385-839d-c9d1aa36b9be
translation-type: tm+mt
source-git-commit: af5201da6eac644e150783195bdbc8f93760c3f1
workflow-type: tm+mt
source-wordcount: '1177'
ht-degree: 63%

---


# 创建客户属性来源并上传数据文件

创建客户属性源（CSV 和 FIN 文件）并上传数据。您可以在做好准备时激活数据源。在数据源激活后，可将属性数据共享到 Analytics 和 Target。

## 客户属性工作流程 {#concept_BF0AF88E9EF841219ED4D10754CD7154}

![](assets/crs.png)

1. [创建数据文件](../attributes/t-crs-usecase.md#task_B5FB8C0649374C7A94C45DCF2878EA1A)
1. [创建属性来源并上传数据文件](../attributes/t-crs-usecase.md#task_09DAC0F2B76141E491721C1E679AABC8)
1. [验证架构](../attributes/t-crs-usecase.md#task_09DAC0F2B76141E491721C1E679AABC8)
1. [配置订阅并激活属性来源](../attributes/t-crs-usecase.md#task_1ACA21198F0E46A897A320C244DFF6EA)

在数据源处于活动状态后，您可以：

* [在Adobe Analytics中使用客户属性](../attributes/t-crs-usecase.md#task_7EB0680540CE4B65911B2C779210915D)
* [在Adobe目标中使用客户属性](../attributes/t-crs-usecase.md#task_FC5F9D9059114027B62DB9B1C7D9E257)

>[!IMPORTANT]
>
>要访问此功能，必须将用户分配到“客户属性”产品配置文件（客户属性 - 默认访问）。导航到 **[!UICONTROL 管理]** > **[!UICONTROL 管理控制台]** > **[!UICONTROL 产]**&#x200B;品。 If *Customer Attributes* displays as one of the [!UICONTROL Product Profiles], you are ready to begin. Users that are added to the Customer Attributes group will see the [!UICONTROL Customer Attributes] menu on the left side of the Experience Cloud interface.
>
>要使用“客户属性”功能，用户还必须属于解决方案级组(Analytics或 [!DNL Target])。

See [Manage Experience Cloud users and products](../admin-getting-started/admin-getting-started.md#task_3295A85536BF48899A1AB40D207E77E9).

## 创建数据文件 {#task_B5FB8C0649374C7A94C45DCF2878EA1A}

此数据是来自您的CRM的企业客户数据。 数据可能包括产品的订阅者数据，包括成员ID、授权产品、最新启动的产品等。

1. 创建一个 `.csv`.

   >[!NOTE]
   >
   >在此过程的后续步骤中，您将拖放此 `.csv` 文件以上传它。然而，如果您[通过 FTP 上传](../attributes/t-upload-attributes-ftp.md#task_591C3B6733424718A62453D2F8ADF73B)，则还需要一个与 `.csv` 文件同名的 `.fin` 文件。

   示例企业客户数据文件：

   ![](assets/01_crs_usecase.png)

1. 在继续操作之前，请先查看[数据文件要求](../attributes/crs-data-file.md#concept_DE908F362DF24172BFEF48E1797DAF19)中的重要信息，然后再上传文件。
1. [创建客户属性来源并上传数据](../attributes/t-crs-usecase.md#task_BCC327B2A0EF4A1BBB2934013AB92B78)，如下所述。

## 创建属性来源并上传数据文件 {#task_09DAC0F2B76141E491721C1E679AABC8}

在 Experience Cloud 的“新建客户属性来源”页面中执行这些步骤。

>[!IMPORTANT]
>
>创建、修改或删除客户属性来源时，大约会有将近一小时的延迟。在此之后，ID 才开始与新的数据源进行同步。您在 Audience Manager 中必须具有管理权限才能创建或修改客户属性来源。联系 Audience Manager 客户关怀团队或咨询以获取管理权限。

1. 在 [!DNL Experience Cloud] 中，单击菜单 ![](assets/menu-icon.png) 图标。
1. Under **[!DNL Experience Platform]**, click **[!UICONTROL People]** > **[!UICONTROL Customer Attributes]**.

   在“[!UICONTROL 客户属性]”页面中，您可以管理和编辑现有的属性数据源。

   ![步骤结果](assets/03_crs_usecase.png)
1. 单击&#x200B;**[!UICONTROL 新建]**。

   ![步骤结果](assets/04_crs_usecase.png)
1. 在“[!UICONTROL 编辑客户属性来源]”页面中，配置以下字段：

   * **[!UICONTROL 名称：]**&#x200B;数据属性来源的易记名称。对于 [!DNL Adobe Target]，属性名称不能包含空格。如果传递包含空格的属性，[!DNL Target] 会将其忽略。其他不受支持的字符包括：`< , >, ', "`。

   * **[!UICONTROL 描述：]**（可选）数据属性来源的描述。

   * **[!UICONTROL 别名 ID：]**&#x200B;表示客户属性数据的来源，如特定的 CRM 系统。在您的客户属性来源代码中使用的唯一 ID。此 ID 应当是唯一的，使用小写字母并且没有空格。在Experience Cloud UI中客户属性源的别名ID字段中输入的值应与从实施中传入的值（无论是通过动态标签管理还是Mobile SDK的JavaScript）相匹配。

      别名ID对应于您设置其他客户ID值的某些区域。 例如：

      * **动态标签管理：** 别名ID与Experience Cloud ID服 *务工具* “客户 [!UICONTROL 设置”下][的“集](https://docs.adobe.com/content/help/zh-Hans/dtm/using/tools/macid.html) 成代码”值相对应。

      * **访客API:** 别名ID与您可以与每 [个访客关](https://docs.adobe.com/content/help/zh-Hans/id-service/using/reference/authenticated-state.html) 联的其他客户ID相对应。

         例如，下面的&#x200B;*“crm_id”*：

         ```
         "crm_id":"67312378756723456"
         ```

      * **iOS:** 别名ID与visitorSyncIdentifiers: *identifiers中* 的“ [idType”相对应](https://docs.adobe.com/content/help/zh-Hans/mobile-services/ios/overview.html)。

         例如：

         `[ADBMobile visitorSyncIdentifiers:@{@<`**`"idType"`**`:@"idValue"}];`

      * **Android:** 别名ID与syncIdentifiers *中的* “idType [”对应](https://docs.adobe.com/content/help/zh-Hans/mobile-services/android/overview.html)。

         例如：

         `identifiers.put(`**`"idType"`**`, "idValue");`

         请参阅[利用多个数据源](../attributes/crs-data-file.md#section_76DEB6001C614F4DB8BCC3E5D05088CB)，以了解有关别名 ID 字段和客户 ID 的数据处理的其他信息。
   * **[!UICONTROL 文件上传：]**&#x200B;您可以拖放 `.csv` 数据文件，或通过 FTP 上传数据。（使用 FTP 还需要 `.fin` 文件。）请参阅[通过 FTP 上传数据](../attributes/t-upload-attributes-ftp.md#task_591C3B6733424718A62453D2F8ADF73B)。

      >[!IMPORTANT]
      >
      >存在特定的数据文件要求。请参阅[数据文件要求](../attributes/crs-data-file.md#concept_DE908F362DF24172BFEF48E1797DAF19)，以了解更多信息。


      上传文件后，表数据将显示在此页 [!UICONTROL 的“文件] 上传”标题下。 您可以验证模式、配置订阅或设置FTP。

      **文件上传图**

      ![](assets/file_upload_attributes.png)

   * **[!UICONTROL 唯一客户 ID：]**&#x200B;显示您向此属性来源上传了多少个唯一 ID。

   * **[!UICONTROL 别名为 Experience Cloud 访客 ID 的客户提供 ID：]**&#x200B;显示别名为 Experience Cloud 访客 ID 的 ID 数量。

   * **[!UICONTROL 具有高别名计数的客户提供 ID：]**&#x200B;显示具有 500 个或更多 Experience Cloud 访客 ID 别名的客户提供 ID 的计数。这些客户提供的ID很可能不代表个人，而是某种共享登录。 系统会将与这些ID关联的属性分发到500个最新的别名Experience Cloud访客ID，直到别名计数达到10,000。 到那时，系统会使客户提供 ID 无效，且不再分发关联的属性。



## 验证架构 {#task_404AAC411B0D4E129AB3AC8B7BE85859}

验证过程允许您将显示名称和描述映射到已上传的属性（字符串、整数、数字等等）。您还可以通过更新架构来删除属性。

请参阅[验证架构](../attributes/validate-schema.md#concept_B3A01A15D04E4F998118E09B3A9B5043)。

要删除属性，请参阅[（可选）更新架构（删除属性）](../attributes/t-crs-usecase.md#task_6568898BB7C44A42ABFB86532B89063C)。

## （可选）更新架构（删除属性）{#task_6568898BB7C44A42ABFB86532B89063C}

如何删除和替换架构中的属性。

1. 在[!UICONTROL 编辑客户属性来源]页面上，删除 **[!UICONTROL Target]** 或 **[!UICONTROL Analytics]** 订阅（位于[!UICONTROL 配置订阅]下）。
1. [上传具有更新字段的新数据文件](../attributes/t-crs-usecase.md#task_09DAC0F2B76141E491721C1E679AABC8)。

## 配置订阅和激活属性来源 {#task_1ACA21198F0E46A897A320C244DFF6EA}

配置订阅可设置Experience Cloud和解决方案之间的数据流。 激活属性源后，数据便可流向订阅的解决方案。 您上传的客户记录将与来自您网站或应用程序的传入ID信号相匹配。

请参阅[配置订阅](../attributes/subscription.md#concept_ECA3C44FA6D540C89CC04BA3C49E63BF)。

**激活属性来源的方法**

在[!UICONTROL 新建[或编辑]客户属性来源]页面上，找到[!UICONTROL 激活]标题，然后单击&#x200B;**[!UICONTROL 活动]**。

![步骤结果](assets/activate_attribute_source.png)

## Use Customer Attributes in Adobe Analytics {#task_7EB0680540CE4B65911B2C779210915D}

通过使用 
<keyword>
Adobe Analytics
</keyword> 等解决方案中现在提供的数据，您可以报告数据、分析数据并在市场营销活动中执行相应的操作。

以下示例显示了一个基于上传属性的 [!DNL Analytics] 区段。This segment shows [!DNL Photoshop Lightroom] subscribers whose most-launched product is Photoshop.

![](assets/08_crs_usecase.png)

当您将区段发布到Experience Cloud时，Experience Cloud受众和受众管理器中会提供该区段。

有关详 [细信息，请参阅](https://docs.adobe.com/help/en/analytics/components/variables/dimensions-reports/reports-customer-attributes.html) “分析”帮助中的“客户属性报告”。

## Use Customer Attributes in Adobe Target {#task_FC5F9D9059114027B62DB9B1C7D9E257}

在 [!DNL Target] 中，您可以在创建受众时从“访客配置文件”区域选择一个客户属性。All Customer Attributes will have the prefix [!DNL crs.] in the list. 可根据需要，将这些属性与其他数据属性结合使用以构建受众。

![](assets/crs-add-attribute-target.png)

请参 [阅帮助中的创建](https://docs.adobe.com/content/help/en/target/using/audiences/create-audiences/audiences.html) 新 [!DNL Target] 受众。
