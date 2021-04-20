---
product: campaign
solution: Campaign
title: 将 IP 范围添加到允许列表
description: 了解如何将 IP 范围添加到 SFTP 服务器访问允许列表
feature: Control Panel
role: Architect
level: Experienced
translation-type: tm+mt
source-git-commit: 4b8020dfd5d1f81a81d0e20025cfabe734744d34
workflow-type: tm+mt
source-wordcount: '636'
ht-degree: 94%

---


# IP 范围允许列表{#ip-range-allow-listing}

>[!CONTEXTUALHELP]
>id="cp_ip_whitelist"
>title="关于 IP 允许列表"
>abstract="在此选项卡中，您可以向允许列表添加 IP 范围，以建立与 SFTP 服务器的连接。此处仅显示您有权访问的 SFTP 服务器。请联系您的管理员以请求访问其他 SFTP 服务器。"
>additional-url="https://images-tv.adobe.com/mpcv3/8a977e03-d76c-44d3-853c-95d0b799c870_1560205338.1920x1080at3000_h264.mp4#t=98" text="观看演示视频"

SFTP 服务器受到保护。为了能够访问这些服务器以查看文件或编写新文件，您需要将访问服务器的系统或客户端的公共 IP 地址添加到允许列表。

![](assets/do-not-localize/how-to-video.png) 使用活动类Campaign Standard在视频中 [发现](https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/sftp-management/adding-ip-range-to-allow-list.html?lang=en#sftp-management) 此功 [能](https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/sftp-management/adding-ip-range-to-allow-list.html?lang=en#sftp-management)

## 关于 CIDR 格式 {#about-cidr-format}

CIDR（无类域间路由）是在控制面板界面中添加 IP 范围时受支持的格式。

语法依次由 IP 地址、“/”字符和十进制数字组成。[本文](https://whatismyipaddress.com/cidr)详细介绍了格式及其语法。

您可以在互联网上搜索免费的在线工具，这些工具将帮助您将现有的 IP 范围转换为 CIDR 格式。

## 最佳做法 {#best-practices}

在控制面板中将 IP 地址添加到允许列表时，请确保遵循以下建议和限制条件。

* **将 IP 范围添加到允许列表**，而不是单个 IP 地址。要将单个 IP 地址添加到允许列表，请在其中附加“/32”，以标识该范围仅包含单个 IP 地址。
* **请勿向允许列表添加非常宽的范围**，例如，包括 > 265 个 IP 地址。控制面板将拒绝任何介于 /0 和 /23 之间的 CIDR 格式范围。
* 只能将&#x200B;**公共 IP 地址**&#x200B;添加到允许列表。
* 请确保&#x200B;**定期从允许列表中**&#x200B;删除不再需要的 IP 地址。

## 向允许列表添加 IP 地址{#adding-ip-addresses-allow-list}

>[!CONTEXTUALHELP]
>id="cp_sftp_iprange_add"
>title="添加新 IP 范围"
>abstract="定义要添加到允许列表以连接到 SFTP 服务器的 IP 范围。"

要向允许列表添加 IP 范围，请执行以下步骤：

1. 打开 **[!UICONTROL SFTP]** 卡，然后选择 **[!UICONTROL IP Allow Listing]** 选项卡。
1. 将为每个实例显示允许列表上的 IP 地址列表。从左侧列表中选择所需的实例，然后单击 **[!UICONTROL Add new IP range]**&#x200B;按钮。

   ![](assets/control_panel_add_range.png)

1. 定义要添加到允许列表的 IP 范围（以 CIDR 格式），然后定义将在列表中显示的标签。

   >[!NOTE]
   >
   >标签字段中允许使用以下特殊字符：
   > `. _ - : / ( ) # , @ [ ] + = & ; { } ! $`

   ![](assets/control_panel_add_range2.png)

   >[!IMPORTANT]
   >
   >IP 范围不能与允许列表上的现有范围重叠。在这种情况下，首先删除包含重叠 IP 的范围。
   >
   >可以在允许列表上为多个实例添加一个范围。为此，请按向下箭头键或键入所需实例的前几个字母，然后从建议列表中选择该实例。

   ![](assets/control_panel_add_range3.png)

1. 单击&#x200B;**[!UICONTROL Save]**&#x200B;按钮。在完全处理请求之前，允许列表的 IP 添加项将显示为“待处理”。此处理操作只需要几秒钟即可完成。

要从允许列表中删除 IP 范围，请选中要删除的 IP 范围，然后单击 **[!UICONTROL Delete IP range]** 按钮。

![](assets/control_panel_delete_range2.png)

>[!NOTE]
>
>当前无法编辑允许列表上的范围。要修改 IP 范围，请将其删除，然后创建一个符合您的需求的 IP 范围。

## 监控更改 {#monitoring-changes}

通过控制面板主页中的 **[!UICONTROL Job Logs]**，您可以监控对允许列表上的 IP 地址所做的所有更改。

有关控制面板界面的详细信息，请参阅[此部分](../../discover/using/discovering-the-interface.md)。

![](assets/control_panel_ip_log.png)
