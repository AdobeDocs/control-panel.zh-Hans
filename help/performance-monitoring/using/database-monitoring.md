---
product: campaign
solution: Campaign
title: 关于数据库监控
description: 了解如何在控制面板中监测 Campaign 数据库
feature: Control Panel, Monitoring
role: Admin
level: Experienced
exl-id: 2bd7d2dd-97be-49bb-9f8e-7161d0742bc1
source-git-commit: a3485766791387bd9422b4f29daf86296efafb98
workflow-type: tm+mt
source-wordcount: '384'
ht-degree: 78%

---

# 关于数据库监控 {#database-monitoring}

## 关于实例数据库 {#about-instances-databases}

根据您的合同，您的每个 Campaign 实例都会配备特定大小的数据库空间。数据库包括存储在 Adobe Campaign 中的所有&#x200B;**资源**、**工作流**&#x200B;和&#x200B;**数据**。

随着时间的推移，数据库会达到其最大容量，尤其是从不删除实例中存储的资源时，或者存在许多处于暂停状态的工作流时。

实例数据库溢出可能导致若干问题（无法登录、无法发送电子邮件等）。因此，监测实例的数据库对于确保最佳性能至关重要。

如果您订阅了 [电子邮件警报](../../performance-monitoring/using/email-alerting.md)，则当实例的一个数据库达到其容量的80%或更多时，您将收到电子邮件通知。

## 监测数据库使用{#monitoring-database-usage}

>[!CONTEXTUALHELP]
>id="cp_performancemonitoring_database"
>title="关于数据库监控"
>abstract="在此选项卡中，您可以获取有关每个 Campaign 实例的最新和历史数据库使用情况及演变的实时信息。"
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/performance-monitoring/about-performance-monitoring.html?lang=zh-Hans" text="关于性能监控"

控制面板允许您监测每个 Campaign 实例的数据库使用情况。为此，请打开 **[!UICONTROL Performance Monitoring]** 信息卡，然后选择 **[!UICONTROL Databases]** 选项卡。

从 **[!UICONTROL Instance List]** 中选择所需的实例，以显示有关该实例的数据库容量和已用空间的信息。

>[!NOTE]
>
>如果控制面板中显示可用的数据库空间大小与合同中规定的大小不一致，请联系客户关怀团队。

![](assets/databases_dashboard.png)

该仪表板中的数据将根据 **[!UICONTROL Database cleanup technical workflow]** 在您的Campaign实例上运行的(请参阅 [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard/using/administrating/application-settings/technical-workflows.html?lang=zh-Hans#list-of-technical-workflows) 和 [Campaign v7/v8](https://experienceleague.adobe.com/docs/campaign-classic/using/monitoring-campaign-classic/data-processing/database-cleanup-workflow.html?lang=zh-Hans) 文档)。 您可以检查工作流上次运行于 **[!UICONTROL Used Space]** 和 **[!UICONTROL Provided Space]** 量度。 请注意，如果工作流已超过 3 天未运行，我们建议您联系 Adobe 客户关怀团队，以便让他们调查工作流未运行的原因。

此仪表板中提供了其他量度，以帮助您分析实例数据库的使用情况。 这些部分详细说明了这些术语：

* [数据库利用率](../../performance-monitoring/using/database-utilization.md)
* [存储概述](../../performance-monitoring/using/database-storage-overview.md)
* [十大临时资源](../../performance-monitoring/using/database-top-ten-resources.md)
* [活动查询](../../performance-monitoring/using/database-active-queries.md)

![](assets/do-not-localize/how-to-video.png)在使用 [Campaign v7/v8](https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/performance-monitoring/monitoring-databases.html?lang=zh-Hans#performance-monitoring) 或 [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/performance-monitoring/monitoring-databases.html?lang=zh-Hans#performance-monitoring) 的视频中了解这一功能
