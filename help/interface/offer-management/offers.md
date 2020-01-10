---
description: 创建和管理要在Adobe Campaign中使用的选件。
seo-description: 创建和管理要在Adobe Campaign中使用的选件。
seo-title: 选件管理
title: 选件管理
uuid: 83e1d4cd-c5fa-4df0-9603-2914eb4648f8
index: y
translation-type: tm+mt
source-git-commit: 55ac24fe0fb177a5a81765af1f7d602acc0f5d0f

---


# 选件

创建和管理要在Adobe Campaign中使用的选件。

选件管理中有两种 [!UICONTROL 选件]:

| 类型 | 描述 |
|---|---|
| 一般优惠 | 允许您填写完整的优惠数据模型（资格规则、开始日期和结束日期以及内容）。 |
| 替代选件 | 如果客户没有资格获得任何其他选定的优惠，则为最后一次优惠。 您不能将任何资格规则或开始日期和结束日期与回退选件相关联。 |

>[!NOTE]
>
>在选件活动中，系统始终会要求您选择回退选件。 因此，在创建选件活动之前，选件库存中必须至少有一个备用选件。

## Create an offer {#task_6C4AE487377D424FA133ACCA6AF741D4}

创建要添加到选件清单的选件。

1. 从选件管理 [!UICONTROL 的] “库存”选 [!UICONTROL 项卡中]，单击 **[!UICONTROL 创建新选件]**，然后选择创建****选件。

   ![](assets/create-offerx.png)

1. 请完成以下字段：

   <table id="table_60A4001CE9F34422ACB59FB62C9CBDCD">
<thead> 
  <tr> 
   <th colname="col1" class="entry"> 字段 </th> 
   <th colname="col2" class="entry"> 描述 </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>选件名称 </p> </td> 
   <td colname="col2"> <p>与选件关联的名称。 您的库存中不能有两个名称重复的选件。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>开始日期 </p> </td> 
   <td colname="col2"> <p>显示选件的日期。 如果选择了1/15/17的开始日期，则可以从1/15/17的凌晨12:00开始显示选件。 </p> <p>促销管理按UTC时间标准运行。 这意味着： </p> <p> 
     <ul id="ul_A9D49B4405F34E6DA8FB52A13437F799"> 
      <li id="li_9490D092B235479A981FC2D5DD0B17B4">优惠在设置为开始的当天00:00 UTC时生效。 </li> 
      <li id="li_C28BB1FEB9E1495593826403CF5F67A9">优惠将于结束日期的后一天00:00 UTC时到期。 例如，如果某个选件的结束日期设置为5/14，则该选件将在5/15的00:00 UTC时过期。 随后将存档选件。 </li> 
      <li id="li_D3F7DCD1BF75410A8F4F5BC468B667AB">在Adobe Campaign中准备电子邮件时，只会显示在该时间点有效的选件。 </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>结束日期 </p> </td> 
   <td colname="col2"> <p>选件结束的日期。 如果选择1/20/17的结束日期，则在1/20/17的11:59PM之后将不再显示选件。 选件通过其结束日期后，会自动将其存档。 </p><p>促销管理按UTC时间标准运行。 有关更多信息，请参阅上面的行。 </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>资格规则 </p> </td> 
   <td colname="col2"> <p>您可以根据Campaign数据库中提供的数据创建选件资格 <span class="keyword"> 规则</span> 。 资格规则确定可向谁显示选件以及何时显示选件。 </p> <p>例如，您可以指定仅希望在(Geder = 'Femule')和(Region = 'Northeast')时显示“Women's Winter Clothing Offer”。 用于构建这些规则的属性来自Campaign standard配置文件。 </p> <p>注意： 首次访问“选件管理”时，规则构建器中没有可用的属性。 您必须从营销活动UI中共享属性。 共享后，这些属性即可用。 </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>最大上限 </p> </td> 
   <td colname="col2"> <p>可建议的最长时间。 </p> <p>注意： 在电子邮件准备时计算建议的次数。 例如，如果您准备了一封包含大量选件的电子邮件，则无论是否发送了该电子邮件，这些数字都会计入您的最大上限。 </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>每用户最大上限 </p> </td> 
   <td colname="col2"> <p>向给定用户建议选件的最长时间。 </p> <p>注意： 在电子邮件准备时计算向给定用户建议的次数。 例如，如果您准备了一封包含大量选件的电子邮件，则无论是否发送了该电子邮件，这些数字都将计入每个用户的最大上限。</p> </td>
  </tr> 
  <tr> 
   <td colname="col1"> <p>标签 </p> </td> 
   <td colname="col2"> <p>向选件添加标签以将其组合在一起。 您可以键入并按Enter键创建新标签，或开始键入内容并从下拉菜单中选择现有选件。 </p> </td> 
  </tr> 
 </tbody> 
</table>

1. 填写表示详细信息。

   | 字段 | 描述 |
   |---|---|
   | Channel | 提供此内容表示的渠道。 Campaign standard电子邮件是当前唯一可用的渠道。 |
   | 版面 | 选择可在其中提供此内容表示的位置。 版面会从“版面”选项卡中预填充。 您必须从下拉菜单中将每个内容表示与位置相关联。 不能在同一选件中使用相同的位置创建多个内容表示形式。 |
   | 内容类型 | 选择图像、图像URL、文本或HTML的内容类型。 |
   | 重定向链接 | 如果您选择图像或图像URL的内容类型，则显示此字段。 如果用户在电子邮件中单击该选件，则会重定向到此链接。 |

1. 单击 **[!UICONTROL 保存并预览]**，以在提交之前查看选件的详细信息。
1. 单击 **[!UICONTROL 批准]**，以批准此选件。 一旦选件处于批准状态，便可在选件活动中使用。

   如果您没有批准选件所需的权限，请改为单击“提 **[!UICONTROL 交”]**。 选件随后将显示在具有待定状态的选件库中。 具有批准权限的用户批准后，它便可用于选件活动。
