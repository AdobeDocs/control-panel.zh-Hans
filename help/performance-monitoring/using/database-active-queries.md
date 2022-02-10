---
product: campaign
solution: Campaign
title: 监测活动查询
description: 了解如何在控制面板中监测 Campaign 实例上的活动查询。
feature: Control Panel
role: Architect
level: Experienced
source-git-commit: 12e9326ba220776874654705587152bf3978949c
workflow-type: ht
source-wordcount: '118'
ht-degree: 100%

---

# 监测活动查询 {#long-running-queries}

**[!UICONTROL Databases]** 选项卡的 **[!UICONTROL Active queries]** 区域列出了在选定实例上运行时间最长的五个查询。

![](assets/active-queries.png)

**[!UICONTROL Duration]** 列指定查询在实例上运行的时长。持续时间以以下格式显示：`hh:mm:ss.ms`。

>[!IMPORTANT]
>
>如果其中一个查询处于活动状态超过 24 小时，而且您订阅了[电子邮件警报](email-alerting.md)，那么您将收到电子邮件通知。
>
>在这种情况下，请联系客户关怀团队，以便他们识别并解决问题。您需要向他们提供 **[!UICONTROL PID]** 列值，这是查询的唯一标识符。
