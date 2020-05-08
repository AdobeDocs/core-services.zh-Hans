---
title: 一般数据保护规定的客户属性支持
description: 一般数据保护规定的客户属性支持
translation-type: tm+mt
source-git-commit: 3a86aed0794c3e35cc028e5bfde5dafcb2285fc8
workflow-type: tm+mt
source-wordcount: '426'
ht-degree: 5%

---


# 一般数据保护规定的客户属性支持


>[!IMPORTANT]
>
>本文档的内容不是法律建议，也不会代替法律建议。请咨询您的法律顾问，以获取有关一般数据保护规定的建议。

2018 [年5月](https://www.adobe.com/privacy/general-data-protection-regulation/what-is-gdpr.html) 25日生效的《一般数据保护规定(GDPR)》(General Data Protection Regulation, GDPR)法律允许欧洲合并(EU)境内的所有个人（数据主体）控制其个人数据，并简化国际业务的监管环境。 本法适用于在处理个人数据时优惠商品或服务到欧盟境内个人、监控其行为或从其收集个人数据的所有企业（数据管理者），无论数据管理者的业务位置如何。

Adobe Experience Cloud充当数据处理者，处理其接收的任何个人数据并代表其客户进行存储。 作为数据管理者，您可以决定Adobe Experience Cloud代表您处理和存储的个人数据。

本文档描述客户属性如何使用Adobe Experience Platform Privacy Service API和隐私服务UI支持数据主体的GDPR数据访问和删除权限。

有关GDPR对您的业务意味着什么的更多信息，请 [参阅GDPR和您的业务](https://www.adobe.com/cn/privacy/general-data-protection-regulation.html)。

## 发送客户属性请求所需的设置

要请求访问和删除客户属性的数据，您需要：

1. 识别以下内容：

* IMS组织ID
* 要执行操作的CRS数据源的别名ID
* 要执行操作的用户档案的CRM ID

IMS组织ID是附加@AdobeOrg的24个字符的字母数字字符串。 如果您的营销团队或内部Adobe系统管理员不知道您组织的IMS组织ID，请通过gdprsupport@adobe.com与Adobe客户服务部门联系。 您需要IMS组织ID向隐私API提交请求。

2. 使用隐私服务UI向客户属性提交访问和删除请求，并检查现有请求的状态。

## 客户属性JSON请求中的必填字段值

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

* “条例”: **gdpr** （适用于请求的隐私法规）

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
