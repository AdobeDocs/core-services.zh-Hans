---
description: 了解如何在 [!DNL Customer Attributes] 中为Analytics和Target配置订阅，以及如何激活数据源。
solution: Experience Cloud
title: 如何在 [!DNL Customer Attributes]中配置订阅
feature: Customer Attributes
topic: Administration
role: Admin
level: Experienced
exl-id: cfa2aa5c-337f-401e-80eb-cbe36cb1d41e
TQID: 'https://experienceleague.adobe.com/SVDhQ4Y2-CIJ7pVhapEqhu1gRkYSrPjmSI8-NejBddI'
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
feature_v2:
  - id: fdbb8fc9-ffa3-4b86-88fe-aa4c5a3e1bc6
subfeature_v2: id:id:
role_v2: id:
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: f01d85af42b8f2c27dbada8f73546bc6fe4bf710
workflow-type: tm+mt
source-wordcount: 408
ht-degree: 47%

---

# 配置客户属性订阅

[!DNL Customer Attributes]订阅允许客户属性数据在CX Enterprise和应用程序（[!DNL Analytics]和[!DNL Target]）之间流动。

例如，Adobe Analytics 订阅允许将属性数据纳入报表中。 如果您使用[!DNL Adobe Target]，则可以上传客户属性以进行定位和分段。

**要配置订阅并激活数据源**

1. 在[!DNL Customer Attributes]中找到您的数据源以进行编辑：

   在[!DNL CX Enterprise]中，单击&#x200B;**[!UICONTROL Apps]** ![菜单](assets/menu-icon.png) > **[!DNL Customer Attributes]**。

1. 在[!UICONTROL Edit Customer Attribute Source]上，单击&#x200B;**[!UICONTROL File Upload]**。

1. 单击 **[!UICONTROL Configure Subscriptions]**。

   ![在CX Enterprise中配置订阅](assets/configure-subscriptions.png)

1. 要激活客户属性来源，请单击&#x200B;**[!UICONTROL Active]**，然后单击&#x200B;**[!UICONTROL Save]**。

1. 要配置[!DNL Analytics]或[!DNL Target]的订阅，请单击&#x200B;**[!UICONTROL Configure]**。

   以下示例显示了[!DNL Target]订阅：

   ![步骤结果](assets/subscription-target.png)

   | 元素 | 描述 |
   | --- | --- |
   | 解决方案 | **Adobe Analytics**<br>&#x200B;选择[!DNL Analytics]，指定要接收属性数据的报表包，以及要包含的属性。<br>**Adobe Target**<br>&#x200B;您可以上传客户属性，以便进行定位和分段。 如果想要基于属性数据来定位测试，或者希望数据在Analytics中可用于分段，则此功能非常有用。<br>登录时，在&#x200B;**[!DNL Target]** > **受众**&#x200B;中，访客的上传客户属性数据可用。<br>支持多个数据源。 在您的网站上设置客户ID后，请确认至少有一个别名已订阅到[!DNL Target]。 |
   | 报表包(Adobe Analytics) | 来自Analytics的报表包。<br>您无法在一个属性来源内向Analytics订阅添加总计10个以上的报表包。 选择要包含的报表包时，请考虑以下建议：<ul><li>选择具有一组共同的已经过身份验证的客户的报表包。 如果一个报表包中的经过身份验证的客户与另一报表包中的经过身份验证的客户不重叠，请将这些报表包分成不同的属性源。</li><li>如果可能，属性源中包含的报表包应具有相似的流量。</li></ul><br>如果您有 10 个以上的报表包具有一组共同的经过身份验证的客户，则可以配置更多的客户属性来源，使每个来源最多包含 10 个报表包。 |
   | 要包含的属性（Analytics 和 [!DNL Target]） | 您希望发送至应用程序的属性。 <br>在配置订阅和选择属性时，根据您拥有的应用程序，_每个报表包_&#x200B;将会受到以下限制：<ul><li>Foundation：0 个</li><li>Select：3 个</li><li>Prime：15 个</li><li>Ultimate：200 个</li><li>Standard：总共允许 3 个</li><li>Premium：每个报表包允许 200 个</li><li>[!DNL Target] Standard：5 个</li><li>[!DNL Target] Premium：200 个</li></ul><br>**注意：**&#x200B;当您升级到 Analytics Premium 时，附加属性会在延迟 24 小时后才可用。 在此延迟期间，您可能会看到属性订阅数量达到最大值错误。 |

1. 单击 **[!UICONTROL Save]**。
