---
description: 了解如何验证Adobe Experience Cloud中的 [!DNL Customer Attributes] 架构。
solution: Experience Cloud
title: 如何验证 [!DNL Customer Attributes] 架构
feature: Customer Attributes
topic: Administration
role: Admin
level: Experienced
exl-id: 776d1fd3-c733-4970-a76b-4c3c0119ee77
source-git-commit: 21120abb5ab0fcc8d556012851548f39f3875038
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 49%

---

# 验证架构

验证过程允许您将显示名称和描述映射到已上传的属性（字符串、整数、数字等）。

将根据这些设置创建架构。该架构用于验证将来上传到此数据源的所有数据。该映射过程不会更改原始数据。

>[!NOTE]
>
>验证后更新架构会删除客户属性。请参阅[更新架构（同时删除属性）](t-crs-usecase.md)。

**验证架构**

1. 在[!DNL Customer Attributes]中，单击要编辑的属性源。

1. 在&#x200B;**[!UICONTROL 编辑客户属性Source]**&#x200B;上，单击&#x200B;**[!UICONTROL 文件上传]**。

1. 在[!UICONTROL 文件上载和架构验证]页面上，单击&#x200B;**[!UICONTROL 操作]** > **[!UICONTROL 查看/编辑架构]**

   ![编辑架构](assets/view_edit_schema.png)

   在[!UICONTROL 编辑架构]页面上，架构的每一行都表示一列上传的CSV文件。

   ![在Experience Cloud中编辑架构页面](assets/edit-schema.png)

**操作**

* **[!UICONTROL 添加数据：]**&#x200B;将新属性数据上传到此数据源。

* **[!UICONTROL 查看/编辑架构：]**&#x200B;将显示名称映射到属性数据，如下一步骤中所述。

* **[!UICONTROL FTP设置：]**&#x200B;创建你的FTP帐户以[通过FTP上载你的数据](t-upload-attributes-ftp.md)（可选）。

* **[!UICONTROL ID查找：]**&#x200B;输入您`.csv`中的客户ID (CID)以查找该ID的Experience Cloud信息。 此功能可用于解决为何属性数据不对访客显示的问题：

   * **[!UICONTROL ECID (Experience Cloud ID)：]**&#x200B;在您使用最新的 Experience Cloud ID 服务时显示。如果您在使用MCID服务，但此处未列出ID，则Experience Cloud尚未收到该CID的别名。 这意味着访客还没有登录，或您的实施没有传递此 ID。

   * **[!UICONTROL CID （客户ID）：]**&#x200B;与此CID关联的属性。 如果您使用 prop 或 eVar 上传 CID (AVID)，并且只看到了显示的属性而没有看到 AVID，这说明访客还没有登录到您的站点。

   * **[!UICONTROL AVID（Analytics 访客 ID）：]**&#x200B;在您使用 prop 或 eVar 上传 CID 时显示。如果这些ID正在传递到Experience Cloud，则与您输入的CID关联的任何访客ID都将显示在此处。
