---
title: 数据库监控
description: 了解如何在控制面板中监视活动库
translation-type: tm+mt
source-git-commit: b2447b30314f4bd46b2b6e144f7f713ff2f1ec59
workflow-type: tm+mt
source-wordcount: '443'
ht-degree: 4%

---


# 数据库监控 {#database-monitoring}

## 关于实例数据库 {#about-instances-databases}

根据您的合同，您的每个活动实例都会配置特定数量的数据库空间。

数据库包 **括存储**&#x200B;在 **Adobe Campaign中** 的所 **有资** 产、工作流和数据。

随着时间的推移，工作流库可以达到其最大容量，尤其是当存储的资源从不从实例中删除时，或者如果存储的资源处于暂停状态，则更是如此。

溢出实例数据库可能导致若干问题（无法登录、发送电子邮件等）。 因此，监控实例的数据库对于确保最佳性能至关重要。

>[!NOTE]
>
>控制面板中显示的数据库空间量可能不反映合同中指定的数据库空间量。 通常，系统会临时为您提供更大的数据库空间，以确保系统性能。

## 监视数据库使用情况 {#monitoring-instances-database}

控制面板允许您监视每个活动实例的数据库使用情况。 为此，请执行以下步骤：

1. 打开 **[!UICONTROL Performance Monitoring]**&#x200B;卡，然后选择 **[!UICONTROL Databases]** 选项卡。

1. 从中选择所需的实例 **[!UICONTROL Instance List]**。

   上部区域提供有关实例的数据库容量和已用空间的信息。

   ![](assets/databases_dashboard.png)

   下面的区域以图形形式表示过去7天内最低、平均和最高数据库利用率，以及90%数据库利用率阈值，用红色虚线曲线表示。

   您可以使用右上角的可用过滤器更改显示的时间段。

   为了更好的可读性，您还可以突出显示图形中的一条或多条曲线。 为此，请从图例中选择 **[!UICONTROL Aggregation Type]** 它们。

   将指针悬停在图形上可获取有关所选时间段的详细信息。

   ![](assets/databases_dashboard_detail.png)

>[!NOTE]
>
>此仪表板之外，您还可以在其中一个数据库达到容量时接收通知。 为此，请订阅电子邮 [件警报](../../performance-monitoring/using/email-alerting.md)

## 防止数据库过载 {#preventing-database-overload}

Campaign Standard和经典优惠防止数据库磁盘空间过度消耗的各种方法。

以下部分提供了活动文档中的有用资源，以帮助您优化数据库使用：

**工作流监控**

* [工作流最佳实践](https://docs.adobe.com/content/help/en/campaign-standard/using/managing-processes-and-data/workflow-general-operation/best-practices-workflows.html) (Campaign Standard)
* [监视工作流执行](https://docs.adobe.com/help/en/campaign-classic/using/automating-with-workflows/monitoring-workflows/monitoring-workflow-execution.html) (Campaign Classic)

**数据库维护**

* 数据库清理技术工作流[程(Campaign Standard](https://docs.adobe.com/help/en/campaign-standard/using/administrating/application-settings/technical-workflows.html#list-of-technical-workflows) / [Campaign Classic](https://docs.adobe.com/help/en/campaign-classic/using/monitoring-campaign-classic/data-processing/database-cleanup-workflow.html))
* [数据库维护指南](https://docs.adobe.com/content/help/en/campaign-classic/using/monitoring-campaign-classic/database-maintenance/recommendations.html) (Campaign Classic)
* [数据库性能疑难解答](https://docs.adobe.com/content/help/en/campaign-classic/using/monitoring-campaign-classic/troubleshooting/database-performances.html) (Campaign Classic)
* [数据库相关选项](https://docs.adobe.com/help/en/campaign-classic/using/installing-campaign-classic/appendices/configuring-campaign-options.html#database) (Campaign Classic)
