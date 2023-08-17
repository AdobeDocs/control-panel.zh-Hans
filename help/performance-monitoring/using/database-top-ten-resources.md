---
product: campaign
solution: Campaign
title: 十大临时资源
description: 了解如何在控制面板中监测Campaign数据库上工作流和投放生成的十大临时资源。
feature: Control Panel
role: Architect
level: Experienced
exl-id: 2fa2ffbb-102b-42c4-8feb-b0263ee9c930
source-git-commit: b17abddf6bad7e58cb7bd825cd97322427a0b21f
workflow-type: tm+mt
source-wordcount: '175'
ht-degree: 69%

---

# 十大临时资源 {#top-10}

**[!UICONTROL Top 10 temporary resources]** 区域列出了工作流和投放生成的十大临时资源。

监测正在创建大型临时资源的工作流和投放是监测数据库的关键步骤。如果任何临时资源占用的数据库空间过多，请确保此工作流或投放是必要的，并最终导航到您的实例以停止它。

>[!IMPORTANT]
>
>一般建议是避免在非开箱即用资源中设置&#x200B;**超过 40 列**。如果发现某个工作流涉及大量图表或占用大量数据库空间，我们建议查看该工作流，以调查它生成如此多数据的原因。
>
>Campaign Standard和Classic指南也在 [此页面](database-preventing-overload.md) 以帮助您防止数据库过载。

![](assets/database-top10.png)

此 **[!UICONTROL View all]** 按钮允许您访问 **[!UICONTROL Storage overview]** 获取有关这些临时资源的详细信息的详细信息。 有关详细信息，请参见[此页面](database-storage-overview.md)。
