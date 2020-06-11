---
title: 活动用户档案监视
description: 了解如何获得有关每个用户档案实例最新和历史活动活动使用情况和演变的实时信息。
translation-type: tm+mt
source-git-commit: 024eb750021ff2446b34d648b5abfb016eabc289
workflow-type: tm+mt
source-wordcount: '389'
ht-degree: 14%

---


# 活动用户档案监视 {#active-profiles-monitoring}

>[!IMPORTANT]
>
>控制面板中的活动用户档案监视功能在测试版中可用，如有频繁更新和修改，恕不另行通知。
>
>该功能适用于在AWS上托管的从Campaign Standard10368构建和Campaign Classic8931构建开始的客户。 如果您使用的是以前的版本，则需要升级才能使用此功能。

## 关于活动用户档案 {#about-active-profiles}

根据您的合同，您的每个活动实例都会配置特定数量的有效用户档案，这些活动会计入账单。 请参阅您的最新合同，了解已购买的有效用户档案数量。

“用户档案”是指代表最终客户或潜在客户的信息记录（例如 nmsRecipient 表或外部表中的记录，包含 cookie ID、客户 ID、移动标识符或与特定渠道相关的其他信息）。

如果用户档案在过去12个月中通过任何渠道被定向或与其联系，则视为积极。

>[!NOTE]
>
>Facebook 和 Twitter 渠道不包含在內。

有关活动用户档案的详细信息，请参 [阅Campaign Standard](https://docs.adobe.com/content/help/en/campaign-standard/using/profiles-and-audiences/managing-profiles/active-profiles.html) 和 [Campaign Classic](https://docs.adobe.com/content/help/en/campaign-classic/using/getting-started/profile-management/about-profiles.html#active-profiles) 文档。

## 监视活动用户档案 {#monitoring-active-profiles}

控制面板允许您监视每个用户档案实例的活动活动使用情况。

为此，请执行以下步骤：

1. 打开 **[!UICONTROL Performance Monitoring]**&#x200B;卡，然后选择 **[!UICONTROL Active Profiles]** 选项卡。

1. 从中选择所需的实例 **[!UICONTROL Instance List]**。

1. 实例使用的活动用户档案数以及实例上次运行计费工作流的时间。

![](assets/active-profiles-graph.png)

>[!NOTE]
>
>活动用户档案基于每天在您的实例上运行的专用技术工作流进行计数：
>
>* Campaign Standard [的“账单](https://docs.adobe.com/help/en/campaign-standard/using/administrating/application-settings/technical-workflows.html) ”工作流、
>* 用于 [Campaign Classic的“活动付费用户档案的](https://docs.adobe.com/content/help/en/campaign-classic/using/automating-with-workflows/technical-workflows/deliveries.html) 数量”工作流。


下面的区域以图形形式显示了过去30天内活动用户档案的使用情况。 您可以使用右上角的可用过滤器将显示的时间段更改为1年。

将指针悬停在某个图形栏上可获得选定时段上使用的活动用户档案的确切数量。
