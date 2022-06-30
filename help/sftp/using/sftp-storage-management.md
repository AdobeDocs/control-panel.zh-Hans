---
product: campaign
solution: Campaign
title: SFTP 存储管理
description: 了解如何监控和管理 SFTP 服务器的存储
feature: Control Panel
role: Architect
level: Experienced
exl-id: eaf67573-f088-47d9-8a25-273d08dc541a
source-git-commit: 8db39899be5dfe610f39a6cecc23bd5f969078c6
workflow-type: tm+mt
source-wordcount: '388'
ht-degree: 75%

---

# SFTP 存储管理 {#sftp-storage-management}

>[!CONTEXTUALHELP]
>id="cp_storage"
>title="关于存储容量"
>abstract="在此选项卡中，您可以查看 SFTP 服务器的存储容量和利用率信息。您还可以通过单击SFTP服务器名称来列出在SFTP服务器上占用最多空间的前10个文件。 此处仅显示您有权访问的 SFTP 服务器。请联系您的管理员以请求访问其他 SFTP 服务器。"
>additional-url="https://images-tv.adobe.com/mpcv3/8a977e03-d76c-44d3-853c-95d0b799c870_1560205338.1920x1080at3000_h264.mp4" text="观看演示视频"

您的 SFTP 服务器上可能配置了不同的存储容量，具体取决于您的合同条款。

您必须定期监控每个 SFTP 服务器的可用空间。否则，您可能无法再在服务器上保存任何其他文件，也无法成功执行依赖此服务器更新的工作流。

![](assets/do-not-localize/how-to-video.png) 使用 [Campaign v7/v8](https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/sftp-management/monitoring-server-capacity.html#sftp-management) 或 [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/sftp-management/monitoring-server-capacity.html#sftp-management)

## 访问存储容量信息 {#accessing-storage-capacity-information}

有关您有权访问的所有实例所使用的空间的信息，请参阅 SFTP 卡的&#x200B;**[!UICONTROL Storage]**&#x200B;选项卡。每次刷新页面时都会更新。

![](assets/control_panel_space.png)

对于每个实例，在其存储超出容量时会向您发出可视警报：

* **橙色**：表示实例超过了其容量的 80%；
* **红色**：表示实例超过了其容量的 90%。

您还可以通过单击SFTP服务器名称来识别在SFTP服务器上占用最多空间的前10个文件。

![](assets/sftp-top10.png)

此外，还提供其他提示，帮助您了解在服务器接近容量时如何继续操作。

## 存储容量耗尽时的最佳做法 {#best-practices-when-capacity-runs-out}

1. **清理 SFTP 服务器的旧文件或不必要的文件**。有关如何访问 SFTP 服务器文件夹的详细信息，请参阅[此部分](../../sftp/using/logging-into-sftp-server.md)。
1. 确保清理 SFTP 服务器的&#x200B;**工作流**&#x200B;成功执行。有关Adobe Campaign中技术工作流的更多信息，请参阅 [Campaign v7/v8](https://experienceleague.adobe.com/docs/campaign-classic/using/automating-with-workflows/advanced-management/about-technical-workflows.html) 和 [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard/using/administrating/application-settings/technical-workflows.html?lang=zh-Hans) 文档。
1. 联系您的客户团队以&#x200B;**请求更多存储**（可能需要额外付费）。
1. 如果您认为存在问题，请联系&#x200B;**客户关怀团队**。
