---
product: campaign
solution: Campaign
title: 活动轮廓监测
description: 了解如何获得有关每个 Campaign 实例最新和历史活动轮廓使用情况和演变的实时信息。
feature: Control Panel, Monitoring
role: Admin
level: Experienced
exl-id: a157cc27-577f-490f-8c4f-0f203219cfb5
source-git-commit: 73cf3102c0926728595e975ee4c85bf110f2a23d
workflow-type: ht
source-wordcount: '418'
ht-degree: 100%

---

# 监测活动轮廓 {#active-profiles-monitoring}

## 关于活动轮廓 {#about-active-profiles}

>[!IMPORTANT]
>
>Beta 版中提供可通过控制面板使用的活动轮廓监测功能，如有频繁更新和修改，恕不另行通知。Campaign Standard 10368 版本提供该功能。

根据您的合同，您的每个 Campaign 实例都会配置特定数量的活动轮廓，并对这些活动轮廓进行计数以计费。请参阅您的最新合同，了解已购买的活动轮廓数量。

“轮廓”是指代表最终客户或潜在客户的信息记录（例如 nmsRecipient 表或外部表中的记录，包含 cookie ID、客户 ID、移动标识符或与特定渠道相关的其他信息）。

如果轮廓在过去 12 个月中通过任何渠道被定向或与其联系，则视为处于活动状态。

>[!NOTE]
>
>不会考虑 Facebook 和 X（以前称为 Twitter）渠道。

有关活动轮廓的详细信息，请参阅 [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard/using/profiles-and-audiences/managing-profiles/active-profiles.html?lang=zh-Hans) 和 [Campaign v7/v8](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/profile-management/about-profiles.html?lang=zh-Hans#active-profiles) 文档。

## 监测活动轮廓使用情况 {#monitoring-active-profiles}

>[!CONTEXTUALHELP]
>id="cp_performancemonitoring_active_profile"
>title="关于活动轮廓监控"
>abstract="在此选项卡中，您可以获取有关每个 Campaign 实例和贵组织的最新和历史活动轮廓使用情况及变化的实时信息。"

要在控制面板中监控活动轮廓的使用情况，请导航至&#x200B;**[!UICONTROL 性能监控]**&#x200B;信息卡 > **[!UICONTROL 活跃轮廓]**&#x200B;选项卡，然后从&#x200B;**[!UICONTROL 实例列表]**&#x200B;中选择所需的实例。

此时将显示有关活动轮廓使用情况的信息。

![](assets/active-profiles-graph.png)

上半部分显示以下信息：

* 所选实例中当前使用的活动轮廓计数，以及实例的最近计费工作流执行的时间戳。

* 贵组织在所有实例中使用的活动轮廓总数。

  >[!NOTE]
  >
  >仅当您有多个与贵组织相关联的实例时，才会显示此部分。

* 分配给贵组织的活动轮廓总数。

下半部分直观地呈现了过去 30 天内活动轮廓的使用情况。您可以使用右上角的筛选条件将此时间范围更改为 1 年。将鼠标悬停在图形上，可获得选定时段使用的活动轮廓的确切数量。

与活动轮廓使用情况相关的信息会根据定期在您的实例上运行的专用 [!DNL Campaign]“计费”技术工作流在控制面板中更新。

| Campaign 版本 | 技术工作流 | 运行 |
|  ---  |  ---  |  ---  |
| Campaign Standard | [计费](https://experienceleague.adobe.com/docs/campaign-standard/using/administrating/application-settings/technical-workflows.html?lang=zh-Hans) | 每日 |
| Campaign v7/v8 | [计费](https://experienceleague.adobe.com/docs/campaign-classic/using/automating-with-workflows/advanced-management/about-technical-workflows.html?lang=zh-Hans) | 每月 |

