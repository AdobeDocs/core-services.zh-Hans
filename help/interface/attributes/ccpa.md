---
title: '客户属性对《加州消费者隐私法案》的支持 '
description: 了解客户属性对《加州消费者隐私法案》的支持
feature: 客户属性
topic: 管理
role: 管理员
level: 富有经验
translation-type: ht
source-git-commit: 61d60273e933c637dfe4400da78257e1c80015b3
workflow-type: ht
source-wordcount: '440'
ht-degree: 100%

---


# 客户属性对《加州消费者隐私法案》的支持

本页面介绍[!UICONTROL 客户属性]对《加州消费者隐私法案》(CCPA) 的支持。

>[!IMPORTANT]
>
>本文档的内容不是法律建议，也不会代替法律建议。请咨询您的法律顾问，以获得有关 (CCPA) 的建议。

CCPA 是加利福尼亚州的新隐私法，于 2020 年 1 月 1 日生效。CCPA 为加利福尼亚州居民提供了有关其个人信息的新权利，并对在加利福尼亚州开展业务的某些实体强加了数据保护责任。CCPA 为消费者提供访问和删除其个人信息的权利，以及选择退出某些有资格将个人信息“出售”给第三方的活动的权利。

作为企业，您可以决定 Adobe Experience Cloud 代表您处理和存储的个人数据。

作为您的服务提供商，Adobe Experience Cloud 将为您的企业提供支持，使其履行 CCPA 规定且适用于 Experience Cloud 产品和服务使用的义务，包括管理有关访问和删除个人信息的请求。

本文档介绍了[!UICONTROL 客户属性]如何使用 Adobe Experience Platform 隐私服务 API 和隐私服务 UI 支持数据主体的 CCPA 数据访问和删除权利。

有关涉及 CCPA 的 Adobe 隐私服务的更多信息，请参阅 [Adobe 隐私中心](https://www.adobe.com/privacy/ccpa.html)。

## 发送[!UICONTROL 客户属性]请求所需的设置

要请求访问和删除[!UICONTROL 客户属性]的数据，您需要：

1. 识别以下内容：

   * IMS 组织 ID
   * 要执行操作的 CRS 数据源的别名 ID
   * 要执行操作的配置文件的 CRM ID

   IMS 组织 ID 是一个由 24 个字符组成的字母数字字符串，其后附加有 @AdobeOrg。如果您的营销团队或内部 Adobe 系统管理员不知道您组织的 IMS 组织 ID，请通过 gdprsupport@adobe.com 与 Adobe 客户关怀团队联系。您需要拥有 IMS 组织 ID 才能向隐私 API 提交请求。

1. 在“[!UICONTROL 隐私服务]”中，您可以向客户属性提交访问和删除请求，并检查现有请求的状态。

## [!UICONTROL 客户属性] JSON 请求中的必填字段值

&quot;company context&quot;：

* &quot;namespace&quot;：**imsOrgID**
* &quot;value&quot;：&lt;*您的 IMS 组织 ID 值*>

&quot;users&quot;：

* &quot;key&quot;：&lt;*通常是客户的名称*>

* &quot;action&quot;：**access** 或 **delete**

* &quot;user IDs&quot;：

   * &quot;namespace&quot;：&lt;*CRS 数据源的别名 ID*>

   * &quot;type&quot;：**integrationCode**

   * &quot;value&quot;：&lt;*CRM ID*>

* &quot;include&quot;：**CRS**（即适用于该请求的 Adobe 产品）

* &quot;regulation&quot;：**ccpa**（即适用于该请求的隐私法规）

## JSON 请求的示例

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

## 针对访问请求返回的数据字段

```
attributes:
{
"value”:<*value*>,
"key”:<*key*>,
"displayName”:<*displayName*>
}
```
