---
product: campaign
solution: Campaign
title: 吞吐量和延迟监测
description: 了解如何在控制面板中监测 Campaign 实例的吞吐量和延迟。
feature: Control Panel
role: Architect
level: Experienced
exl-id: eddef17f-0667-4b43-bc56-2b1aeeae61bb
source-git-commit: 84fe0aeb10bc5e535a7ab54a3316a51a1a32b3ca
workflow-type: tm+mt
source-wordcount: '314'
ht-degree: 73%

---

# 吞吐量和延迟监测 {#throughputs-latency-monitoring}

>[!CONTEXTUALHELP]
>id="cp_performancemonitoring_throughputslatencies"
>title="关于吞吐量和延迟监测 "
>abstract="在此选项卡中，您可以监测在实例上一段时间内的投放吞吐量和延迟趋势。"

控制面板允许您监控每个实例的投放吞吐量和延迟。

>[!IMPORTANT]
>
>此功能适用于所有Campaign Standard和v8客户，以及版本号为9032、9330、9346或9349的Campaign V7客户 [独立](https://experienceleague.adobe.com/docs/campaign-classic/using/installing-campaign-classic/deployment-types-/standalone-deployment.html) 部署（不含任何mid实例）。

监测一段时间内的投放吞吐量和延迟趋势对于了解实例的使用情况并确保它们正常运行至关重要。

可在控制面板的 **[!UICONTROL Throughputs & Latency]** 选项卡，**[!UICONTROL Performance Monitoring]** 信息卡中查看每个 Campaign 实例的此类信息（请注意，控制面板可能需要长达 1 小时才能显示相关数字）。

* **[!UICONTROL Throughput]** 区域提供您有权访问的所有通信渠道的、从选定的 Campaign 实例每小时发送的消息数的相关信息。

   >[!NOTE]
   >
   >对于Campaign v7/v8，显示的吞吐量数是从MID（中间采购）实例实现的吞吐量。 对于独立营销(MKT)部署（不含任何MID实例），将显示MKT实例的吞吐量。

* **[!UICONTROL Latency]** 区域提供发送实时事务型通信时在选定实例上遇到的延迟的相关信息。延迟的捕获和显现位置为第 95 和第 99 个百分位数，这意味着 95% 和 99% 的请求应比给定的延迟更快。

![](assets/throughput-latencies-overview.png)

>[!NOTE]
>
>此区域中显示的所有数字都是近似的，仅供参考。

默认情况下，将显示当天的数据。您可以使用 **[!UICONTROL 6 months]**、**[!UICONTROL 30 days]** 和 **[!UICONTROL 7 days]** 按钮更改显示的时间段。

您还可以使用可排序的列而非图形，以表格格式显示信息。为此，请单击 **[!UICONTROL Visualization settings]** 按钮，然后选择 **[!UICONTROL Table]**。

![](assets/throughput-latencies-table.png)
