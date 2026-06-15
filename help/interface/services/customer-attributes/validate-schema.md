---
description: 了解如何验证Adobe CX Enterprise中的 [!DNL Customer Attributes] 架构。
solution: Experience Cloud
title: 如何验证 [!DNL Customer Attributes] 架构
feature: Customer Attributes
topic: Administration
role: Admin
level: Experienced
exl-id: 776d1fd3-c733-4970-a76b-4c3c0119ee77
TQID: https://experienceleague.adobe.com/J-AaDn4HtD1bS-VCPn2XiPLVBbTnYyl5o1NpJ9HFj1g
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
feature_v2:
  - id: fdbb8fc9-ffa3-4b86-88fe-aa4c5a3e1bc6
subfeature_v2:
  - id: b75843fa-0a67-4a44-a6b1-cc627b0481dc
  - id: fef08361-6ac5-460c-93fe-d063e40b6a49
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 50012e2564e88e1a6e16578e3331136c7df0cb21
workflow-type: tm+mt
source-wordcount: 345
ht-degree: 39%

---

# 验证架构

验证过程允许您将显示名称和描述映射到已上传的属性（字符串、整数、数字等等）。

将根据这些设置创建架构。 该架构用于验证将来上传到此数据源的所有数据。 该映射过程不会更改原始数据。

>[!NOTE]
>
>验证后更新架构会删除客户属性。 请参阅[更新架构（同时删除属性）](t-crs-usecase.md)。

**验证架构**

1. 在[!DNL Customer Attributes]中，单击要编辑的属性源。

1. 在&#x200B;**[!UICONTROL 编辑客户属性Source]**&#x200B;上，单击&#x200B;**[!UICONTROL 文件上传]**。

1. 在[!UICONTROL 文件上载和架构验证]页面上，单击&#x200B;**[!UICONTROL 操作]** > **[!UICONTROL 查看/编辑架构]**

   ![编辑架构](assets/actions.png)

   在[!UICONTROL 编辑架构]页面上，架构的每一行都表示一列上传的CSV文件。

   ![在CX Enterprise中编辑架构页](assets/schema-edit.png)

**操作**

* **[!UICONTROL 添加数据：]**&#x200B;将新属性数据上载到此数据源。

* **[!UICONTROL 查看/编辑架构：]**&#x200B;将显示名称映射到属性数据，如下一步骤中所述。

* **[!UICONTROL FTP设置：]**&#x200B;创建你的FTP帐户以[通过FTP上载你的数据](t-upload-attributes-ftp.md)（可选）。

* **[!UICONTROL ID查找：]**&#x200B;输入您`.csv`中的客户ID (CID)以查找该ID的CX Enterprise信息。 此功能可用于解决为何属性数据不对访客显示的问题：

   * **[!UICONTROL ECID (CX Enterprise ID)：]**&#x200B;在您使用最新的CX Enterprise ID服务时显示。 如果您在MCID服务上，但此处未列出ID ，则CX Enterprise尚未收到该CID的别名。 这意味着访客还没有登录，或您的实施没有传递此 ID。

   * **[!UICONTROL CID （客户ID）：]**&#x200B;与此CID关联的属性。 如果您使用 prop 或 eVar 上传 CID (AVID)，并且只看到了显示的属性而没有看到 AVID，这说明访客还没有登录到您的站点。

   * **[!UICONTROL AVID （Analytics访客ID）：]**&#x200B;在您使用prop或eVar上传CID时显示。 如果这些ID正在传递到CX Enterprise，则与您输入的CID关联的任何访客ID都将显示在此处。
