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
source-wordcount: '433'
ht-degree: 41%

---

# 监测活动用户档案 {#active-profiles-monitoring}

## 关于活动用户档案 {#about-active-profiles}

>[!IMPORTANT]
>
>测试版中提供控制面板的活动用户档案监控，如有频繁更新和修改，恕不另行通知。它可以从Campaign Standard10368构建中使用。

根据您的合同，您的每个 Campaign 实例都会配置特定数量的活动用户档案，并对这些活动用户档案进行计数以计费。请参阅您的最新合同，了解已购买的活动用户档案数量。

“用户档案”是指代表最终客户或潜在客户的信息记录（例如 nmsRecipient 表或外部表中的记录，包含 cookie ID、客户 ID、移动标识符或与特定渠道相关的其他信息）。

如果用户档案在过去 12 个月中通过任何渠道被定向或与其联系，则视为处于活动状态。

>[!NOTE]
>
>Facebook 和 Twitter 渠道不包含在內。

有关活动用户档案的详细信息，请参阅 [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard/using/profiles-and-audiences/managing-profiles/active-profiles.html) 和 [Campaign v7/v8](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/profile-management/about-profiles.html#active-profiles) 文档。

## 监测活动用户档案使用情况 {#monitoring-active-profiles}

>[!CONTEXTUALHELP]
>id="cp_performancemonitoring_active_profile"
>title="关于活跃配置文件监控"
>abstract="在此选项卡中，您可以获取有关您的Campaign实例和组织中每个用户档案的最新和历史活动用户档案使用和演变的实时信息。"

与活动用户档案使用相关的信息基于专用的控制面板更新 [!DNL Campaign] 每天在实例上运行的技术工作流：
* Campaign Standard 的[“计费](https://experienceleague.adobe.com/docs/campaign-standard/using/administrating/application-settings/technical-workflows.html?lang=zh-Hans)”工作流，
* 此 [&quot;有效计费用户档案数&quot;](https://experienceleague.adobe.com/docs/campaign-classic/using/automating-with-workflows/advanced-management/about-technical-workflows.html?lang=zh-Hans) Campaign v7/v8的工作流。


要监控控制面板中活动用户档案的使用情况，请导航至 **[!UICONTROL Performance Monitoring]** 信息卡> **[!UICONTROL Active Profiles]** 选项卡，然后从中选择所需的实例 **[!UICONTROL Instance List]**.

此时将显示有关使用活动用户档案的信息。

![](assets/active-profiles-graph.png)

上半部分显示以下信息：

* 选定实例中当前使用的活动用户档案计数，以及实例最近计费工作流执行的时间戳。

* 您的组织在所有实例中使用的活动配置文件总数。

  >[!NOTE]
  >
  >仅当您有多个与组织关联的实例时，此部分才可见。

* 分配给贵组织的活动用户档案总数。

下部分直观地呈现过去30天内活动用户档案的使用情况。 您可以使用右上角的过滤器将此时间范围更改为1年。 将鼠标悬停在图形上可获得选定时段使用的活动用户档案的确切数量。
