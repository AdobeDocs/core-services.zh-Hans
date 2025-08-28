---
description: 了解如何通过FTP将客户属性数据上传到Experience Cloud。
solution: Experience Cloud
title: 通过FTP上传客户属性数据文件
feature: Customer Attributes
topic: Administration
role: Admin
level: Experienced
exl-id: ed9e4a8f-493a-4a0f-a87e-674c7da95b99
source-git-commit: 21120abb5ab0fcc8d556012851548f39f3875038
workflow-type: tm+mt
source-wordcount: '378'
ht-degree: 67%

---

# 通过FTP上传数据文件（可选）

如果您不使用拖放操作上传，则可以通过FTP将客户属性数据上传到Experience Cloud。

在Experience Cloud中创建客户属性来源和FTP帐户后，您可以上传数据。 为每个属性来源创建一个 FTP 帐户。上传的文件存储在该帐户的根文件夹中。该数据必须为 `.csv` 格式，并利用第二个 `.fin` 文件指示上传已完成。

>[!IMPORTANT]
>
>在上传文件之前，先查看[上传客户属性的数据文件要求](crs-data-file.md)。

可以通过FTP或SFTP将文件上传到客户属性FTP站点：

* 您需要支持 SFTP 连接的客户端。
* 您可以使用用户名/密码连接到 SFTP，也可以不使用密码连接到 SFTP，如[此处](https://experienceleague.adobe.com/docs/analytics/export/ftp-and-sftp/secure-file-transfer-protocol/ftp-sftp-cert-auth.html)所示。

**通过 FTP 上传数据文件的方法**

1. [创建客户属性来源并上传数据文件...](t-crs-usecase.md).

   确保您已登录位于 `ftp.adobe.com/<sftpname>` 的 FTP 站点。

1. 单击&#x200B;**[!UICONTROL 操作]** > **[!UICONTROL 文件上传]**。

1. 上传 `.fin` 文件，以便您的文件可被检索到。

   文件类型 `.fin` 是由用户创建的，表示上传已完成。它可以是一个空白的记事本文件。例如，如果您上传 `crs123.csv`，同时也会上传 `crs123.fin`。

   如果上传成功，则两个文件都会移到名为&#x200B;**已处理**&#x200B;的文件夹。

   请参阅[上传客户属性的数据文件要求](crs-data-file.md)，以了解有关文件名和结构的重要信息。

## 设置FTP帐户

为每个属性来源设置一个FTP帐户。

在[!UICONTROL 文件上载和架构验证]页面上，单击&#x200B;**[!UICONTROL FTP设置]**。

![编辑架构](assets/ftp-account.png)

上传的文件存储在该帐户的根文件夹中。该数据必须为 `.csv` 格式，并利用第二个 `.fin` 文件指示上传已完成。

指定给字符串、整数和数字的名称会用于创建 [!DNL Analytics] 指标。

* 从上载的&#x200B;**[!UICONTROL 文件中读取的]**&#x200B;属性：`.csv`属性数据。

* **[!UICONTROL 类型：]**&#x200B;数据类型，例如：

   * **字符串：**&#x200B;字符序列。

   * **整数：**&#x200B;整数。

   * **数字：**&#x200B;最多可以保留两位小数。

* **[!UICONTROL 显示名称：]**&#x200B;属性的易记名称。例如，您可以将属性&#x200B;*客户年龄*&#x200B;更改为&#x200B;*客户自*&#x200B;起。

* **[!UICONTROL 描述：]**&#x200B;属性的易懂描述。