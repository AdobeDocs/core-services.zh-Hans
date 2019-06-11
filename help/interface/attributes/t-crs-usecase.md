---
description: 创建客户属性来源并上传数据。
keywords: 客户属性；核心服务
seo-description: 创建客户属性来源并上传数据。
seo-title: 创建客户属性来源并上传数据文件
solution: Experience Cloud
title: 创建客户属性来源并上传数据文件
uuid: 53dca789-9a91-4385-839d-c9 d1 aa36 b9
translation-type: tm+mt
source-git-commit: b6058194725c3ad50d280a3daad737cd53416204

---


# 创建客户属性来源并上传数据文件

创建客户属性来源并上传数据。可以在准备就绪后激活数据源。在数据源激活后，可将属性数据共享到 Analytics 和 Target。

## 客户属性工作流程 {#concept_BF0AF88E9EF841219ED4D10754CD7154}

![](assets/crs.png)

1. [创建数据文件](../attributes/t-crs-usecase.md#task_B5FB8C0649374C7A94C45DCF2878EA1A)
1. [创建属性来源并上传数据文件](../attributes/t-crs-usecase.md#task_09DAC0F2B76141E491721C1E679AABC8)
1. [验证架构](../attributes/t-crs-usecase.md#task_09DAC0F2B76141E491721C1E679AABC8)
1. [配置订阅并激活属性来源](../attributes/t-crs-usecase.md#task_1ACA21198F0E46A897A320C244DFF6EA)


在数据源处于活动状态后，您可以：

* [在 Adobe Analytics 中使用客户属性](../attributes/t-crs-usecase.md#task_7EB0680540CE4B65911B2C779210915D)
* [在 Adobe Target 中使用客户属性](../attributes/t-crs-usecase.md#task_FC5F9D9059114027B62DB9B1C7D9E257)



>[!IMPORTANT]
>
>要访问此功能，必须将用户分配到客户属性产品配置文件(客户属性-默认访问权限)。( **[!UICONTROL “管理]** ”&gt;“ **[!UICONTROL 管理控制台]** ”&gt;“ **[!UICONTROL 用户]** &gt;”)。添加到客户属性群组的用户将会在 Experience Cloud 界面左侧的“[!UICONTROL 受众]”中看到“[!UICONTROL 客户属性]”菜单项。
>
>此外，还要求具备解决方案群组成员资格。

要使用“客户属性”功能，用户必须属于用户管理中的 Adobe 客户属性群组，并且属于解决方案级别的群组（Analytics 或 Target）。

请参阅[用户和群组](../admin-getting-started/admin-getting-started.md#task_3295A85536BF48899A1AB40D207E77E9)。

## 创建数据文件 {#task_B5FB8C0649374C7A94C45DCF2878EA1A}

此数据是来自您的 CRM 的企业客户数据。此数据可能包含产品的订阅者数据，如成员 ID、获得授权的产品、启动最多的产品等等。


1. 创建一个 [!DNL .csv].


   >[!NOTE]
   >
   >在此过程中，您将拖放以 [!DNL .csv] 上传文件。但是，如果您 [通过FTP上传](../attributes/t-upload-attributes-ftp.md#task_591C3B6733424718A62453D2F8ADF73B)，则还需要具有 [!DNL .fin] 与该名称相同的名称的文件 [!DNL .csv]。



   示例企业客户数据文件：

   ![](assets/01_crs_usecase.png)

1. 在上传文件之前，请先查看 [“数据文件要求”](../attributes/crs-data-file.md#concept_DE908F362DF24172BFEF48E1797DAF19)中的重要信息。
1. [创建客户属性源并上传数据](../attributes/t-crs-usecase.md#task_BCC327B2A0EF4A1BBB2934013AB92B78)，如下所述。

## 创建属性来源并上传数据文件 {#task_09DAC0F2B76141E491721C1E679AABC8}

在 Experience Cloud 的“新建客户属性来源”页面中执行这些步骤。


>[!IMPORTANT]
>
>创建、修改或删除客户属性源时，在ID与新数据源同步之前，最长可延迟一个小时。您必须拥有Audience Manager中的管理权限才能创建或修改客户属性源。联系Audience Manager客户服务或咨询以获得管理权限。


1. 在 [!DNL Experience Cloud]中，单击菜单 ![](assets/menu-icon.png) 图标。
1. 单击 **[!UICONTROL 人物]**，然后单击 **[!UICONTROL 客户属性]**。

   在“[!UICONTROL 客户属性]”页面中，您可以管理和编辑现有的属性数据源。

   ![步骤结果](assets/03_crs_usecase.png)
1. 单击 **[!UICONTROL “新建]**”。

   ![步骤结果](assets/04_crs_usecase.png)
1. 在“[!UICONTROL 编辑客户属性来源]”页面中，配置以下字段：


   * **[!UICONTROL 名称：]** 数据属性源的友好名称。对于 [!DNL Adobe Target]，属性名称不能包含空格。如果传递了空格的属性，则 [!DNL Target] 忽略该属性。不支持的其他字符包括： `< , >, ', "`。

   * **[!UICONTROL 描述：]** (可选)数据属性源的描述。

   * **[!UICONTROL 别名ID：]** 表示客户属性数据的来源，如特定CRM系统。在您的客户属性来源代码中使用的唯一 ID。此 ID 应当是唯一的，使用小写字母并且没有空格。在“别名 ID”字段中为 Experience Cloud UI 的客户属性来源输入的值应当匹配从实施传入的值（无论是通过动态标签管理还是 Mobile SDK 的 JavaScript）。

      别名 ID 对应在其中设置其他客户 ID 值的特定区域。例如：

      * **动态标签管理：** 别名ID对应于Experience *Cloud* ID服务工具 [!UICONTROL 中客户设置][下的集成代码值](https://marketing.adobe.com/resources/help/en_US/dtm/?f=macid) 。

      * **访客 API：** 别名 ID 对应可与每个访客关联的其他[客户 ID](https://marketing.adobe.com/resources/help/en_US/mcvid/?f=mcvid_customer_ids)。

         例如， *“crm_ id”* ：


         ```
         "crm_id":"67312378756723456"
         ```


      * **iOS：** Alias *ID对应于seitorSyncidentifiors* 中 [的“idType”：](https://marketing.adobe.com/resources/help/en_US/mobile/ios/?f=methods)标识符。

         例如：

         `[ADBMobile visitorSyncIdentifiers:@{@<`**`"idType"`**`:@"idValue"}];`


      * **Android：** 别名 ID 对应*Syncidentifiers* 中 [的“idType”](https://marketing.adobe.com/resources/help/en_US/mobile/android/?f=methods)。

         例如：

         `identifiers.put(`**`"idType"`**`, "idValue");`

         有关Alias ID字段和客户ID的数据处理的其他信息，请参阅 [利用多个](../attributes/crs-data-file.md#section_76DEB6001C614F4DB8BCC3E5D05088CB) 数据源。
   * **[!UICONTROL 文件上传：]** 您可以拖放 [!DNL .csv] 数据文件，或通过FTP上传数据。(使用FTP也需要 [!DNL .fin] 文件。)请参阅 [通过FTP上传数据](../attributes/t-upload-attributes-ftp.md#task_591C3B6733424718A62453D2F8ADF73B)。


      >[!IMPORTANT]
      >
      >存在特定的数据文件要求。有关更多信息，请参阅 [数据文件要求](../attributes/crs-data-file.md#concept_DE908F362DF24172BFEF48E1797DAF19) 。


      上传文件之后，表格数据显示在此页面的“[!UICONTROL 文件上传]”标题下方。您可以验证架构，配置订阅或设置 FTP。



      **文件上传图形**

      ![](assets/file_upload_attributes.png)

   * **[!UICONTROL 唯一客户ID：]** 显示上传到此属性源的唯一ID数。

   * **[!UICONTROL 客户提供的ID别名为Experience Cloud访客ID：]** 显示已将多少ID别名为Experience Cloud访客ID。

   * **[!UICONTROL 客户提供的具有高别名计数的ID：]** 显示由500个或更多别名的Experience Cloud访问者ID提供的客户提供的ID计数。这些客户提供 ID 很可能不表示个人而表示某类共享登录。系统将与这些 ID 关联的属性分发给 500 个最近的 Experience Cloud 访客 ID 别名，直到别名计数达到 10,000 为止。到那时，系统会使客户提供 ID 无效，且不再分发关联的属性。










## 验证架构 {#task_404AAC411B0D4E129AB3AC8B7BE85859}

验证过程允许您将显示名称和描述映射到已上传的属性（字符串、整数、数字等等）。您还可以通过更新架构删除属性。

请参阅 [验证架构](../attributes/validate-schema.md#concept_B3A01A15D04E4F998118E09B3A9B5043)。

要删除属性，请参阅 [(可选)更新架构(删除属性)](../attributes/t-crs-usecase.md#task_6568898BB7C44A42ABFB86532B89063C)。

## (可选)更新架构(删除属性) {#task_6568898BB7C44A42ABFB86532B89063C}

如何删除属性并替换架构中的属性。


1. 在 [!UICONTROL “编辑客户属性源] ”页面上，删除 **[!UICONTROL Target]** 或 **[!UICONTROL Analytics]** 订阅( [!UICONTROL 在“配置订阅]”下)。
1. [上传具有更新字段](../attributes/t-crs-usecase.md#task_09DAC0F2B76141E491721C1E679AABC8)的新数据文件。

## 配置订阅和激活属性来源 {#task_1ACA21198F0E46A897A320C244DFF6EA}

配置订阅可设置 Experience Cloud 和各解决方案之间的数据流。激活属性来源允许数据流动到订阅的解决方案。由您上传的客户记录与您的网站或应用程序中传入的 ID 信号匹配。

请参阅 [配置订阅](../attributes/subscription.md#concept_ECA3C44FA6D540C89CC04BA3C49E63BF)。

**激活属性来源的方法**

在[！UICCONTRL创建新 [或编辑] 客户属性源页面，找到 [!UICONTROL 激活] 标题，然后单击 **[!UICONTROL 活动]**。

![步骤结果](assets/activate_attribute_source.png)

## 在 Adobe Analytics 中使用客户属性 {#task_7EB0680540CE4B65911B2C779210915D}

现在，这些数据在解决方案中可用
<keyword>
Adobe Analytics
</keyword>您可以报告数据、分析数据，并在营销活动中采取适当措施。

以下示例显示了一个基于上传属性的 [!DNL Analytics] 区段。此区段显示最常启动产品为 Photoshop 的 Photoshop Lightroom 订阅者。

![](assets/08_crs_usecase.png)

当您将区段发布到Experience Cloud时，Experience Cloud受众和Audience Manager中便会提供该区段。

请参阅 Analytics 帮助中的[客户属性报表](https://marketing.adobe.com/resources/help/en_US/reference/?f=reports_customer_attributes)，以了解详细信息。

## 在 Adobe Target 中使用客户属性 {#task_FC5F9D9059114027B62DB9B1C7D9E257}

在 Target 中，您可以在创建受众时，从“访客配置文件”部分选择客户属性。所有客户属性将在列表 [!DNL crs.] 中包含前缀。可根据需要，将这些属性与其他数据属性结合使用以构建受众。

![](assets/crs-add-attribute-target.png)

请参阅 Target 帮助中的[新建受众](https://marketing.adobe.com/resources/help/en_US/target/target/?f=t_creating_a_new_audience)。
