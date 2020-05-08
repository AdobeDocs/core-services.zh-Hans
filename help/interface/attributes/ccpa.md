---
title: 加利福尼亚消费者隐私法的客户属性支持
description: 加利福尼亚消费者隐私法的客户属性支持
translation-type: tm+mt
source-git-commit: 8709449909ce4fbd441d77fb4bbfb0b7758e805d
workflow-type: tm+mt
source-wordcount: '433'
ht-degree: 4%

---


# 加利福尼亚消费者隐私法的客户属性支持

本页介绍 [!UICONTROL 对California Consumer Privacy Act] (CCPA)的客户属性支持。

>[!IMPORTANT]
>
>本文档的内容不是法律建议，也不会代替法律建议。请咨询您的法律顾问，以获得有关(CCPA)的建议。

CCPA是加利福尼亚州的新隐私法，自2020年1月1日起生效。 CCPA为加利福尼亚州居民提供了有关其个人信息的新权利，并对在加利福尼亚开展业务的某些实体强加数据保护责任。 CCPA为消费者提供访问和删除其个人信息的权利，以及对符选择退出合“向第三方销售”个人信息资格的特定活动的权利。

作为企业，您将代表您确定Adobe Experience Cloud处理和存储的个人数据。

作为您的服务提供商,Adobe Experience Cloud为您的企业提供支持，使其履行CCPA规定的适用于使用Experience Cloud产品和服务的义务，包括管理访问和删除个人信息的请求。

本文档介 [!UICONTROL 绍了客户属性] 如何使用Adobe Experience Platform隐私服务API和隐私服务UI支持数据主体的CCPA数据访问和删除权限。

有关CCPA的Adobe隐私服务的更多信息，请参 [阅Adobe隐私中心](https://www.adobe.com/privacy/ccpa.html)。

## 发送客户属性请求所需 [!UICONTROL 的设置]

要请求访问和删除客户属 [!UICONTROL 性的数]据，您需要：

1. 识别以下内容：

   * IMS组织ID
   * 要执行操作的CRS数据源的别名ID
   * 要执行操作的用户档案的CRM ID
   IMS组织ID是附加@AdobeOrg的24个字符的字母数字字符串。 如果您的营销团队或内部Adobe系统管理员不知道您组织的IMS组织ID，请通过gdprsupport@adobe.com与Adobe客户服务部门联系。 您需要IMS组织ID向隐私API提交请求。

1. 在隐 [!UICONTROL 私服务]中，您可以向客户属性提交访问和删除请求，并检查现有请求的状态。

## 客户属性JSON请 [!UICONTROL 求中的] “必需”字段值

“公司上下文”:

* “命名空间”: **imsOrgID**
* “值”: &lt;*您的IMS组织ID值*>

“用户”:

* “键”: &lt;*通常是客户的名称*>

* “操作”: 访 **问** 或删 **除**

* “用户ID”:

   * “命名空间”: &lt;*CRS数据源的别名ID*>

   * “类型”: **integrationCode**

   * “值”: &lt;*CRM ID*>

* “include”: **CRS** （即适用于请求的Adobe产品）

* “条例”: **ccpa** （适用于请求的隐私法规）

## JSON请求示例

```
{
  "companyContexts": [
    {
      "namespace": "imsOrgID",
      "value": "<IMS_ORG_ID>"
    }
  ],
  "users": [
    {
      "key": "<KEY>",
      "action": [
        "<access/delete>"
      ],
      "userIDs": [
        {
          "namespace": "<Alias ID of CRS Data Source>",
          "type": "integrationCode",
          "value": "<CRM ID>"
        }
      ]
    }
  ],
  "regulation": "<gdpr/ccpa/pdpa>",
  "include": [
    "CRS"
  ]
}
```

## 为访问请求返回的数据字段

```
attributes:
{
"value”:<*value*>,
"key”:<*key*>,
"displayName”:<*displayName*>
}
```
