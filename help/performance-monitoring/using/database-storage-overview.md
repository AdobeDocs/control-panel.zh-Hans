---
product: campaign
solution: Campaign
title: 存储概述
description: 了解如何在控制面板中监控占用实例数据库空间的不同Campaign资源。
feature: Control Panel
role: Architect
level: Experienced
exl-id: bb9e1ce3-2472-4bc1-a82a-a301c6bf830e
source-git-commit: c52094b8145bdd84aa9e71430a811b8a7b32354d
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 59%

---

# 存储概述 {#storage-overview}

>[!CONTEXTUALHELP]
>id="cp_dbdetails_storagedetails"
>title="关于存储概述"
>abstract="在此选项卡中，您可以获取有关占用数据库空间的不同 Campaign 资源的详细信息。"

**[!UICONTROL Storage overview]** 区域以图表形式呈现以下资源所占空间：

* **[!UICONTROL System resources]**

   请注意，如果系统资源占用了大部分数据库空间，我们建议您联系客户关怀团队。

* 您的 Campaign 实例默认提供的 **[!UICONTROL Out-of-the-box tables]**，
* 由工作流和投放创建的 **[!UICONTROL Temporary tables]**，
* 创建自定义资源后生成的 **[!UICONTROL Non-out of the box tables]**。

![](assets/database-storage-overview.png)

单击 **[!UICONTROL View details]** 按钮可获取有关占用数据库空间的不同资源的更多详细信息。

您可以使用下拉列表仅从特定资产类型（工作流、投放、收件人）优化搜索和显示表。

![](assets/database-storage-details.png)

请注意，此屏幕还允许您监视可能需要特定注意的工作流参数，以避免实例上出现任何问题。 请参阅[此页面](workflow-monitoring.md)以了解详情。
