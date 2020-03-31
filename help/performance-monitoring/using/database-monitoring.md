---
title: 数据库监控
description: 了解如何在控制面板中监视活动数据库
translation-type: tm+mt
source-git-commit: f995e0dc51fd95d00fdcaa2eb347b2aedfdef60d

---


# 数据库监控 {#database-monitoring}

## 关于实例数据库 {#about-instances-databases}

根据您的合同，您的每个活动实例都会配置特定数量的数据库空间。

数据库包括 **存储在****Adobe Campaign中的所** 有资 **源、工作流和数据** 。

随着时间的推移，数据库可以达到其最大容量，特别是当存储的资源从未从实例中删除时，或者如果处于暂停状态的工作流很多时。

溢出实例数据库可能导致多个问题（无法登录、发送电子邮件等）。 因此，监控实例的数据库对于确保最佳性能至关重要。

>[!NOTE]
>
>请注意，当前数据库空间容量与合同中指定的不同时间段的数量之间可能存在一些差异，以确保更高的性能。

## 监视数据库使用情况 {#monitoring-instances-database}

1. 打开卡 **[!UICONTROL Health Monitoring]** ，然后选择选 **[!UICONTROL Databases]** 项卡。

1. 从中选择所需的实例 **[!UICONTROL Instance List]**。

   上部区域提供有关实例的数据库容量和使用空间的信息。

   ![](assets/databases_dashboard.png)

   下方区域以图形形式显示了过去7天内数据库的使用情况。 您可以使用右上角的可用过滤器更改显示的时间段。

   将指针悬停在图形上可获取有关所选时间段的详细信息。

   ![](assets/databases_dashboard_detail.png)

## 防止数据库过载 {#preventing-database-overload}

Campaign Standard和经典优惠防止数据库磁盘空间过度消耗的各种方法。

以下部分提供了活动文档中的有用资源，以帮助您优化数据库使用：

**工作流监控**

* [工作流最佳做法](https://docs.adobe.com/content/help/en/campaign-standard/using/managing-processes-and-data/workflow-general-operation/best-practices-workflows.html) (Campaign Standard)
* [监视工作流执行](https://docs.adobe.com/help/en/campaign-classic/using/automating-with-workflows/monitoring-workflows/monitoring-workflow-execution.html) (Campaign Classic)

**数据库维护**

* 数据库清理技术工作流([Campaign Standard](https://docs.adobe.com/help/en/campaign-standard/using/administrating/application-settings/technical-workflowshtml#list-of-technical-workflows) / [Campaign Classic](https://docs.adobe.com/help/en/campaign-classic/using/monitoring-campaign-classic/data-processing/database-cleanup-workflow.html))
* [数据库维护指南](https://docs.adobe.com/content/help/en/campaign-classic/using/monitoring-campaign-classic/database-maintenance/recommendations.html) (Campaign Classic)
* [数据库性能疑难解答](https://docs.adobe.com/content/help/en/campaign-classic/using/monitoring-campaign-classic/troubleshooting/database-performances.html) (Campaign Classic)
* [数据库相关选项](https://docs.adobe.com/help/en/campaign-classic/using/installing-campaign-classic/appendices/configuring-campaign-options.html#database) (Campaign Classic)
