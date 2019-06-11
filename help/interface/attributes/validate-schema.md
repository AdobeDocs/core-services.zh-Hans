---
description: 验证过程允许您将显示名称和描述映射到已上传的属性（字符串、整数、数字等等）。架构是基于这些设置创建的。架构用于验证未来所有上传到此数据源的数据。此映射过程不更改原始数据。
keywords: 客户属性；核心服务
seo-description: 验证过程允许您将显示名称和描述映射到已上传的属性（字符串、整数、数字等等）。架构是基于这些设置创建的。架构用于验证未来所有上传到此数据源的数据。此映射过程不更改原始数据。
seo-title: 验证架构
solution: Experience Cloud
title: 验证架构
uuid: 163a4dbe-d60 b-4089-8ff8-65f7461 fbdf7
translation-type: tm+mt
source-git-commit: 979b2202a70e2a5362aa86a65a17d7c4279b3a1a

---


# 验证架构

验证过程允许您将显示名称和描述映射到已上传的属性（字符串、整数、数字等等）。架构是基于这些设置创建的。架构用于验证未来所有上传到此数据源的数据。此映射过程不更改原始数据。


>[!NOTE]
>
>验证后更新架构将删除客户属性。请参阅 [更新架构(还删除属性)](../attributes/t-crs-usecase.md#task_6568898BB7C44A42ABFB86532B89063C)。


**[!UICONTROL 客户属性源]** &gt; **[!UICONTROL 创建新客户属性源]** &gt; **[!UICONTROL 查看/编辑架构]**

![](assets/view_edit_schema.png)

在“[!UICONTROL 验证架构]”页面中，架构的每一行都表示一列上传的 CSV 文件。

![](assets/06_crs_usecase.png)

* **[!UICONTROL 添加数据：]** 将新属性数据上传到此数据源。

* **[!UICONTROL 查看/编辑架构：]** 映射会显示属性数据的名称，如下一步所述。

* **[!UICONTROL FTP设置：]**[通过FTP上传数据](../attributes/t-upload-attributes-ftp.md#task_591C3B6733424718A62453D2F8ADF73B)。

* **[!UICONTROL ID查找：]** 输入您的客户ID(CID)，查找ID的Experience [!DNL .csv] Cloud信息。此功能可用于解决为何属性数据不对访客显示的问题：

   * **[!UICONTROL MCID(Experience Cloud ID)：]** 显示是否使用最新的Experience Cloud ID服务。如果您在使用 MCID 服务，但这里没有列出 ID，则表示 Experience Cloud 还未收到此 CID 对应的别名。这意味着访客还没有登录，或您的实施没有传递此 ID。

   * **[!UICONTROL CID(客户ID)：]** 与此CID关联的属性。如果您使用 prop 或 eVar 上传 CID (AVID)，并且只看到了显示的属性而没有看到 AVID，这说明访客还没有登录到您的站点。

   * **[!UICONTROL AVID(Analytics访客ID)：]** 显示是否使用prop或eVar上传CID。如果这些 ID 被传递到 Experience Cloud，则与您输入的 CID 关联的所有访客 ID 都将在此处显示。






当您在 Experience Cloud 中创建客户属性来源和 FTP 帐户后，还可以通过 FTP 上传数据。您可以针对每个属性来源创建一个 FTP 帐户。已上传的文件存储在该帐户的根文件夹中。该数据必须为 .csv 格式，并通过另一个 .fin 文件指示上传已完成

您应用于字符串、整数和数字的名称用于创建 [!DNL Analytics] 指标。请参阅 帮助中的[客户属性报表](https://marketing.adobe.com/resources/help/en_US/reference/?f=reports_customer_attributes)，以了解详细信息。[!DNL Analytics]

* **[!UICONTROL 属性：]** 从已上传 [!DNL .csv] 文件读取的属性数据。

* **[!UICONTROL 类型：]** 数据类型，如：

   * **String：** 字符序列。

   * **Integers：** 整数。

   * **Numbers：** 最多可有两位小数。




* **[!UICONTROL 显示名称：]** 属性的友好名称。例如，您可以从客户年龄更改为 ***客户*年龄。

* **[!UICONTROL 描述：]** 属性的友好描述。



