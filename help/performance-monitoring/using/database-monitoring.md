---
product: campaign
solution: Campaign
title: 数据库监控
description: 了解如何在控制面板中监视活动数据库
translation-type: tm+mt
source-git-commit: 2d84a5ebe8dbf42264c94f882a51180aae2a58a6
workflow-type: tm+mt
source-wordcount: '936'
ht-degree: 0%

---


# 数据库监控 {#database-monitoring}

## 关于实例数据库{#about-instances-databases}

根据您的合同，您的每个活动实例都会配置特定数量的数据库空间。

数据库包括以Adobe Campaign存储的所有&#x200B;**assets**、**工作流**&#x200B;和&#x200B;**数据**。

随着时间的推移，工作流库可以达到其最大容量，尤其是当存储的资源从不从实例中删除时，或者如果存储的资源处于暂停状态，则更是如此。

溢出实例数据库可能导致若干问题（无法登录、发送电子邮件等）。 因此，监控实例的数据库对于确保最佳性能至关重要。

>[!NOTE]
>
>如果控制面板中提供的数据库空间数量不反映合同中指定的数量，请联系客户服务。

## 监视数据库使用情况{#monitoring-instances-database}

![](assets/do-not-localize/how-to-video.png) 使用活动类Campaign Standard在视频中 [发](https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/performance-monitoring/monitoring-databases.html?lang=en#performance-monitoring) 现此功 [能](https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/performance-monitoring/monitoring-databases.html?lang=en#performance-monitoring)

控制面板允许您监视每个活动实例的数据库使用情况。 为此，请打开&#x200B;**[!UICONTROL Performance Monitoring]**&#x200B;卡，然后选择&#x200B;**[!UICONTROL Databases]**&#x200B;选项卡。

从&#x200B;**[!UICONTROL Instance List]**&#x200B;中选择所需的实例，以显示有关该实例的数据库容量和已用空间的信息。

![](assets/databases_dashboard.png)

>[!NOTE]
>
>请注意，此仪表板中的数据将根据运行在活动实例上的&#x200B;**[!UICONTROL Database cleanup technical workflow]**&#x200B;更新(请参阅[Campaign Standard](https://docs.adobe.com/help/en/campaign-standard/using/administrating/application-settings/technical-workflows.html#list-of-technical-workflows)和[Campaign Classic](https://docs.adobe.com/help/en/campaign-classic/using/monitoring-campaign-classic/data-processing/database-cleanup-workflow.html)文档)。
>
>您可以检查工作流在&#x200B;**[!UICONTROL Used Space]**&#x200B;和&#x200B;**[!UICONTROL Provided Space]**&#x200B;度量下的上次运行时间。 请注意，如果工作流自3天以来未运行，我们建议联系Adobe客户关怀团队，以便他们调查工作流为何未运行。

本仪表板中提供了下述其他度量，帮助您分析实例数据库的使用情况：

* [数据库利用率](../../performance-monitoring/using/database-monitoring.md#database-utilization)
* [存储概述](../../performance-monitoring/using/database-monitoring.md#storage-overview)
* [十大临时资源](../../performance-monitoring/using/database-monitoring.md#top-10)

### 数据库利用率{#database-utilization}

**[!UICONTROL Database utilization]**&#x200B;区域以图形形式表示过去7天内最低、平均和最高数据库利用率，以及由红色虚线曲线表示的90%数据库利用率阈值。

要更改时间段，请使用图形右上角的可用过滤器。

为了更好的可读性，您还可以突出显示图形中的一条或多条曲线。 为此，请从&#x200B;**[!UICONTROL Aggregation Type]**&#x200B;图例中选择它们。

有关特定时间段的更多详细信息，请将指针悬停在图形上以显示有关此时数据库使用情况的信息。

![](assets/databases_dashboard_detail.png)

### 存储概述{#storage-overview}

**[!UICONTROL Storage overview]**&#x200B;区域以图形形式表示以下用户所占用的空间：

* **[!UICONTROL System resources]**

   请注意，如果系统资源占用了大部分数据库空间，我们建议联系客户关怀。

* **[!UICONTROL Out-of-the-box tables]** 默认情况下，
* **[!UICONTROL Temporary tables]** 由工作流和投放创造，
* **[!UICONTROL Non-out of the box tables]** 创建自定义资源后生成。

![](assets/database-storage-overview.png)

单击&#x200B;**[!UICONTROL View details]**&#x200B;按钮可获取有关占用数据库空间的不同资产的更多详细信息。

![](assets/database-storage-details.png)

使用过滤器仅从特定资产类型调整搜索和显示表。

![](assets/database-storage-overview-filter.png)

### 前10个临时资源{#top-10}

**[!UICONTROL Top 10 temporary resources]**&#x200B;区域列表工作流和投放生成的10大临时资源。

监视正在创建大型临时资源的工作流和投放是监视数据库的关键步骤。 如果任何临时资源占用的投放库空间过多，请确保需要具有此工作流或数据，并最终导航到您的实例以停止它。

>[!IMPORTANT]
>
>一般建议是避免在非开箱资源中具有&#x200B;**超过40列**。

![](assets/database-top10.png)

>[!NOTE]
>
>如果发现工作流具有大量表计数或数据库大小，我们建议查看该工作流，以调查它为何生成如此多的数据。
>
>Campaign Standard和经典资源也在本页末尾提供，以帮助您防止数据库过载。

**[!UICONTROL View all]**&#x200B;按钮允许您访问这些临时资源的详细信息。

![](assets/database-top10-view.png)

>[!NOTE]
>
>**[!UICONTROL Keep interim results]**&#x200B;列中的值指示活动中是启用(&quot;1&quot;)还是禁用(&quot;0&quot;)选项。 **[!UICONTROL Keep interim results]**&#x200B;选项可在工作流属性中访问。 它允许您保存工作流各活动之间过渡的结果(请参阅[Campaign Standard](https://docs.adobe.com/content/help/en/campaign-standard/using/managing-processes-and-data/executing-a-workflow/managing-execution-options.html)和[Campaign Classic](https://docs.adobe.com/content/help/en/campaign-classic/using/automating-with-workflows/general-operation/workflow-best-practices.html#logs)文档)。
>
>如果为某个工作流启用了此选项，则数据库清理工作流将无法回收临时结果占用的空间。 因此，我们建议查看工作流以检查选项是否可以关闭。

## 防止数据库过载{#preventing-database-overload}

Campaign Standard和经典优惠防止数据库磁盘空间过度消耗的各种方法。

以下部分提供了活动文档中的有用资源，以帮助您优化数据库使用：

**工作流监控**

* [工作流最佳实践](https://docs.adobe.com/content/help/en/campaign-standard/using/managing-processes-and-data/workflow-general-operation/best-practices-workflows.html) (Campaign Standard)
* [监视工作流执行](https://docs.adobe.com/help/en/campaign-classic/using/automating-with-workflows/monitoring-workflows/monitoring-workflow-execution.html) (Campaign Classic)

**数据库维护**

* Campaign Standard库清除技术工作流程([](https://docs.adobe.com/help/en/campaign-standard/using/administrating/application-settings/technical-workflows.html#list-of-technical-workflows) / [Campaign Classic](https://docs.adobe.com/help/en/campaign-classic/using/monitoring-campaign-classic/data-processing/database-cleanup-workflow.html))
* [数据库维护指南](https://docs.adobe.com/content/help/en/campaign-classic/using/monitoring-campaign-classic/database-maintenance/recommendations.html) (Campaign Classic)
* [数据库性能疑难解答](https://docs.adobe.com/content/help/en/campaign-classic/using/monitoring-campaign-classic/troubleshooting/database-performances.html) (Campaign Classic)
* [数据库相关选项](https://docs.adobe.com/help/en/campaign-classic/using/installing-campaign-classic/appendices/configuring-campaign-options.html#database) (Campaign Classic)
* 数据保留([Campaign Standard](https://docs.adobe.com/help/en/campaign-standard/using/administrating/application-settings/data-retention.html) / [Campaign Classic](https://docs.adobe.com/help/en/campaign-classic/using/configuring-campaign-classic/data-model/data-model-best-practices.html#data-retention))

>[!NOTE]
>
>此外，当您的某个数据库达到其容量时，您可以接收通知。 为此，请订阅[电子邮件警报](../../performance-monitoring/using/email-alerting.md)。
