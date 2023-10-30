---
product: campaign
solution: Campaign
title: 活动用户档案监控
description: 了解如何获得有关每个 Campaign 实例最新和历史活动用户档案使用情况和演变的实时信息。
feature: Control Panel, Monitoring
role: Admin
level: Experienced
exl-id: a157cc27-577f-490f-8c4f-0f203219cfb5
source-git-commit: a3485766791387bd9422b4f29daf86296efafb98
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# 监测活动用户档案 {#active-profiles-monitoring}

## 关于活动用户档案 {#about-active-profiles}

>[!IMPORTANT]
>
>Beta 版中提供可通过控制面板使用的活动用户档案监测功能，如有频繁更新和修改，恕不另行通知。Campaign Standard 10368 版本提供该功能。

根据您的合同，您的每个 Campaign 实例都会配置特定数量的活动用户档案，并对这些活动用户档案进行计数以计费。请参阅您的最新合同，了解已购买的活动用户档案数量。

“用户档案”是指代表最终客户或潜在客户的信息记录（例如 nmsRecipient 表或外部表中的记录，包含 cookie ID、客户 ID、移动标识符或与特定渠道相关的其他信息）。

如果用户档案在过去 12 个月中通过任何渠道被定向或与其联系，则视为处于活动状态。

>[!NOTE]
>
>Facebook 和 Twitter 渠道不包含在內。

有关活动用户档案的详细信息，请参阅 [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard/using/profiles-and-audiences/managing-profiles/active-profiles.html?lang=zh-Hans) 和 [Campaign v7/v8](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/profile-management/about-profiles.html?lang=zh-Hans#active-profiles) 文档。

## 监测活动用户档案使用情况 {#monitoring-active-profiles}

>[!CONTEXTUALHELP]
>id="cp_performancemonitoring_active_profile"
>title="关于活动用户档案监测"
>abstract="在此选项卡中，您可以获取有关每个 Campaign 实例和贵组织的最新和历史活动用户档案使用情况及变化的实时信息。"

与活动用户档案使用情况相关的信息会根据每天在您的实例上运行的专用 [!DNL Campaign] 技术工作流程在控制面板中更新：
* Campaign Standard 的[“计费”](https://experienceleague.adobe.com/docs/campaign-standard/using/administrating/application-settings/technical-workflows.html?lang=zh-Hans)工作流，
* Campaign v7/v8 的[“活动计费用户档案数量”](https://experienceleague.adobe.com/docs/campaign-classic/using/automating-with-workflows/advanced-management/about-technical-workflows.html?lang=zh-Hans)工作流。


要在控制面板中监测活动用户档案的使用情况，请导航至“**[!UICONTROL Performance Monitoring]**”信息卡 >“**[!UICONTROL Active Profiles]**”选项卡，然后从&#x200B;**[!UICONTROL Instance List]**&#x200B;中选择所需的实例。

此时将显示有关活动用户档案使用情况的信息。

![](assets/active-profiles-graph.png)

上半部分显示以下信息：

* 所选实例中当前使用的活动用户档案计数，以及实例的最近计费工作流执行的时间戳。

* 贵组织在所有实例中使用的活动用户档案总数。

  >[!NOTE]
  >
  >仅当您有多个与贵组织相关联的实例时，才会显示此部分。

* 分配给贵组织的活动用户档案总数。

下半部分直观地呈现了过去 30 天内活动用户档案的使用情况。您可以使用右上角的筛选条件将此时间范围更改为 1 年。将鼠标悬停在图形上，可获得选定时段使用的活动用户档案的确切数量。
