---
description: 了解如何验证 Adobe Experience Cloud 中的客户属性架构。
solution: Experience Cloud
title: 如何验证客户属性架构
feature: Customer Attributes
topic: Administration
role: Admin
level: Experienced
exl-id: 776d1fd3-c733-4970-a76b-4c3c0119ee77
source-git-commit: 2f126877f6a5f090884ebe093f35e4f6d90b4df6
workflow-type: tm+mt
source-wordcount: '451'
ht-degree: 72%

---

# 验证架构

验证过程允许您将显示名称和描述映射到已上传的属性（字符串、整数、数字等等）。将根据这些设置创建架构。该架构用于验证将来上传到此数据源的所有数据。该映射过程不会更改原始数据。

>[!NOTE]
>
>验证后更新架构会删除客户属性。请参阅[更新架构（同时删除属性）](t-crs-usecase.md)。

**[!UICONTROL 客户属性Source]** > **[!UICONTROL 新建客户属性Source]** > **[!UICONTROL 查看/编辑架构]**

![编辑架构](assets/view_edit_schema.png)

在[!UICONTROL 验证架构]页面中，架构的每一行都表示一列上传的 CSV 文件。

![验证 Experience Cloud 中的架构页面](assets/06_crs_usecase.png)

* **[!UICONTROL 添加数据：]**&#x200B;将新属性数据上传到此数据源。

* **[!UICONTROL 查看/编辑架构：]**&#x200B;将显示名称映射到属性数据，如下一步骤中所述。

* **[!UICONTROL FTP 设置：]**&#x200B;[通过 FTP 上传数据](t-upload-attributes-ftp.md)。

* **[!UICONTROL ID查找：]**&#x200B;输入您`.csv`中的客户ID (CID)以查找该ID的Experience Cloud信息。 此功能可用于解决为何属性数据不对访客显示的问题：

   * **[!UICONTROL ECID (Experience Cloud ID)：]**&#x200B;在您使用最新的 Experience Cloud ID 服务时显示。如果您在使用MCID服务，但此处未列出ID，则Experience Cloud尚未收到该CID的别名。 这意味着访客还没有登录，或您的实施没有传递此 ID。

   * **[!UICONTROL CID （客户ID）：]**&#x200B;与此CID关联的属性。 如果您使用 prop 或 eVar 上传 CID (AVID)，并且只看到了显示的属性而没有看到 AVID，这说明访客还没有登录到您的站点。

   * **[!UICONTROL AVID（Analytics 访客 ID）：]**&#x200B;在您使用 prop 或 eVar 上传 CID 时显示。如果这些ID正在传递到Experience Cloud，则与您输入的CID关联的任何访客ID都将显示在此处。

在Experience Cloud中创建客户属性来源和FTP帐户后，您还可以通过FTP上传数据。 为每个属性来源创建一个 FTP 帐户。上传的文件存储在该帐户的根文件夹中。该数据必须为 `.csv` 格式，并利用第二个 `.fin` 文件指示上传已完成。

指定给字符串、整数和数字的名称会用于创建 [!DNL Analytics] 指标。

* 从上载的`.csv`文件中读取的&#x200B;**[!UICONTROL 属性：]**&#x200B;属性数据。

* **[!UICONTROL 类型：]**&#x200B;数据类型，例如：

   * **字符串：**&#x200B;字符序列。

   * **整数：**&#x200B;整数。

   * **数字：**&#x200B;最多可以保留两位小数。

* **[!UICONTROL 显示名称：]**&#x200B;属性的易记名称。例如，您可以将属性&#x200B;*客户年龄*&#x200B;更改为&#x200B;*客户自*&#x200B;起。

* **[!UICONTROL 描述：]**&#x200B;属性的易懂描述。
