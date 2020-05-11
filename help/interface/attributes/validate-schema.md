---
description: 验证过程允许您将显示名称和描述映射到已上传的属性（字符串、整数、数字等等）。将根据这些设置创建模式。 该模式用于验证将来上载到此数据源的所有数据。 此映射过程不会更改原始数据。
keywords: Customer Attributes;core services
seo-description: 验证过程允许您将显示名称和描述映射到已上传的属性（字符串、整数、数字等等）。将根据这些设置创建模式。 该模式用于验证将来上载到此数据源的所有数据。 此映射过程不会更改原始数据。
seo-title: 验证架构
solution: Experience Cloud
title: 验证架构
uuid: 163a4dbe-d60b-4089-8ff8-65f7461fbdf7
translation-type: tm+mt
source-git-commit: 0bc7032d0052ba03beac1140dfbfd630e1802bfd
workflow-type: tm+mt
source-wordcount: '551'
ht-degree: 51%

---


# 验证架构

验证过程允许您将显示名称和描述映射到已上传的属性（字符串、整数、数字等等）。将根据这些设置创建模式。 该模式用于验证将来上载到此数据源的所有数据。 此映射过程不会更改原始数据。

>[!NOTE]
>
>验证后更新模式将删除客户属性。 请参阅[更新架构（同时删除属性）](../attributes/t-crs-usecase.md#task_6568898BB7C44A42ABFB86532B89063C)。

**[!UICONTROL 客户属性来源]** > **[!UICONTROL 新建客户属性来源]** > **[!UICONTROL 视图/编辑模式]**

![](assets/view_edit_schema.png)

在“[!UICONTROL 验证架构]”页面中，架构的每一行都表示一列上传的 CSV 文件。

![](assets/06_crs_usecase.png)

* **[!UICONTROL 添加数据：]**&#x200B;将新属性数据上传到此数据源。

* **[!UICONTROL 查看/编辑架构：]**&#x200B;将显示名称映射到属性数据，如下一步骤中所述。

* **[!UICONTROL FTP 设置：]**[通过 FTP 上传数据](../attributes/t-upload-attributes-ftp.md#task_591C3B6733424718A62453D2F8ADF73B)。

* **[!UICONTROL ID 查找：]**&#x200B;输入客户 ID (CID)，从 `.csv` 查找有关此 ID 的 Experience Cloud 信息。此功能可用于解决为何属性数据不对访客显示的问题：

   * **[!UICONTROL ECID(Experience Cloud ID):]** 显示您是否正在使用最新的Experience Cloud ID服务。 如果您在MCID服务上，但此处未列出ID，则Experience Cloud尚未收到该CID的别名。 这意味着访客还没有登录，或您的实施没有传递此 ID。

   * **[!UICONTROL CID（客户 ID）：]**&#x200B;与此 CID 关联的属性。如果您使用 prop 或 eVar 上传 CID (AVID)，并且只看到了显示的属性而没有看到 AVID，这说明访客还没有登录到您的站点。

   * **[!UICONTROL AVID（Analytics 访客 ID）：]**&#x200B;在您使用 prop 或 eVar 上传 CID 时显示。如果这些ID被传递到Experience Cloud，则与您输入的CID关联的任何访客ID都将显示在此处。

在Experience Cloud中创建客户属性源和FTP帐户后，您还可以通过FTP上传数据。 每个属性源创建一个FTP帐户。 上传的文件存储在该帐户的根文件夹中。 数据必须采用。csv格式，并辅以另一个。fin文件以指示上载已完成

指定给字符串、整数和数字的名称会用于创建 [!DNL Analytics] 量度。有关详 [细信息，请参阅](https://docs.adobe.com/help/en/analytics/components/variables/dimensions-reports/reports-customer-attributes.html)[!DNL Analytics] 帮助中的客户属性报告。

* **[!UICONTROL 属性：]**&#x200B;从上传的 `.csv` 文件中读取的属性数据。

* **[!UICONTROL 类型：]**&#x200B;数据类型，例如：

   * **字符串：** 字符序列。

   * **整数：** 全数。

   * **数字：** 最多可以有两位小数。

* **[!UICONTROL 显示名称：]**&#x200B;属性的易记名称。例如，您可以从&#x200B;*客户年龄*&#x200B;更改为&#x200B;*自从以下时间以来的客户*。

* **[!UICONTROL 描述：]**&#x200B;属性的易懂描述。
