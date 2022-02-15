---
product: campaign
solution: Campaign
title: 十大临时资源
description: 了解如何在控制面板中监控由Campaign数据库上的工作流和投放生成的10个最大的临时资源。
feature: Control Panel
role: Architect
level: Experienced
source-git-commit: 34af1000aeb444b273ade358eb35096bd3365fc7
workflow-type: tm+mt
source-wordcount: '283'
ht-degree: 92%

---

# 十大临时资源 {#top-10}

**[!UICONTROL Top 10 temporary resources]** 区域列出了工作流和投放生成的十大临时资源。

监测正在创建大型临时资源的工作流和投放是监测数据库的关键步骤。如果任何临时资源占用的数据库空间过多，请确保此工作流或投放是必要的，并最终导航到您的实例以停止它。

>[!IMPORTANT]
>
>一般建议是避免在非开箱即用资源中设置&#x200B;**超过 40 列**。

![](assets/database-top10.png)

>[!NOTE]
>
>如果发现某个工作流涉及大量图表或占用大量数据库空间，我们建议查看该工作流，以调查它生成如此多数据的原因。
>
>Campaign Standard 和 Classic 资源也会在本页末尾显示，以帮助您防止数据库过载。

点击 **[!UICONTROL View all]** 按钮可访问这些临时资源的详细信息。

![](assets/database-top10-view.png)

**[!UICONTROL Keep interim results]** 列中的值表示该选项在 Campaign 中是启用（“1”）还是禁用（“0”）。这个选项允许您保存工作流的各个活动之间的过渡结果（请参阅 [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard/using/managing-processes-and-data/executing-a-workflow/managing-execution-options.html?lang=zh-Hans) 和 [Campaign Classic](https://experienceleague.adobe.com/docs/campaign-classic/using/automating-with-workflows/introduction/workflow-best-practices.html?lang=zh-Hans#logs) 文档）。

>[!IMPORTANT]
>
>不得在生产工作流中勾选此选项。它用于分析结果，并且是仅为测试目的而设计，因此只能用于开发或暂存环境。
>
>如果控制面板中的值表明，已为某个工作流启用此选项，我们强烈建议在 Campaign 中关闭此选项。
