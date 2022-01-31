---
product: campaign
solution: Campaign
title: 吞吐量和延迟监控
description: 了解如何在控制面板中监控Campaign实例的吞吐量和延迟。
feature: Control Panel
role: Architect
level: Experienced
exl-id: bb9e1ce3-2472-4bc1-a82a-a301c6bf830e
source-git-commit: cbc068c921d0d16b49c881693e44e1ba2a90d015
workflow-type: tm+mt
source-wordcount: '218'
ht-degree: 0%

---

# 吞吐量和延迟监控 {#throughputs-latency-monitoring}

>[!CONTEXTUALHELP]
>id="cp_performancemonitoring_throughputslatencies"
>title="关于吞吐量和延迟监控 "
>abstract="在此选项卡中，您可以监控实例一段时间内的投放流量和延迟趋势。"

监控一段时间内交付流量和延迟趋势对于了解实例的使用情况并确保它们正常运行至关重要。

此信息可在控制面板中为 **[!UICONTROL Performance Monitoring]** 卡片， **[!UICONTROL Throughputs & Latencies]** 选项卡。

>[!NOTE]
>
>此区域中显示的所有数字都是近似的，仅供参考。

![](assets/throughput-latencies-overview.png)

默认情况下，将显示当天的数据。 您可以使用 **[!UICONTROL 6 months]**, **[!UICONTROL 30 days]** 和 **[!UICONTROL 7 days]** 按钮。

的 **[!UICONTROL Throughput]** 区域提供有关您有权访问的所有通信渠道的选定Campaign实例每小时发送的消息数的信息。

您还可以使用可排序列而不是图形以表格格式显示此信息。 为此，请单击 **[!UICONTROL Visualization settings]** 按钮，然后选择 **[!UICONTROL Table]**.

![](assets/throughput-latencies-table.png)

的 **[!UICONTROL Latency]** 区域提供有关发送实时事务型通信时在选定实例上遇到的延迟的信息。 延迟的捕获和显示时间为第95和第99个百分位数，这意味着95%和99%的请求应比给定的延迟更快。

![](assets/throughput-latencies-latency.png)