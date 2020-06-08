---
title: 将 IP 范围列入白名单
description: 了解如何将 IP 范围列入白名单以获取 SFTP 服务器访问权限
translation-type: ht
source-git-commit: a2c19296894ff893987290cb287dc7002ab999e5
workflow-type: ht
source-wordcount: '521'
ht-degree: 100%

---


# 将 IP 范围列入白名单 {#ip-range-whitelisting}

>[!CONTEXTUALHELP]
>id="cp_ip_whitelist"
>title="关于将 IP 列入白名单"
>abstract="在此选项卡中，您可以将 IP 范围列入白名单，以建立与 SFTP 服务器的连接。此处仅显示您有权访问的 SFTP 服务器。请联系您的管理员以请求访问其他 SFTP 服务器。"
>additional-url="https://images-tv.adobe.com/mpcv3/8a977e03-d76c-44d3-853c-95d0b799c870_1560205338.1920x1080at3000_h264.mp4#t=98" text="观看演示视频"

SFTP 服务器受到保护。为了能够访问这些服务器以查看文件或编写新文件，您需要将访问服务器的系统或客户端的公共 IP 地址列入白名单。

## 关于 CIDR 格式 {#about-cidr-format}

CIDR（无类域间路由）是在控制面板界面中添加 IP 范围时受支持的格式。

语法依次由 IP 地址、“/”字符和十进制数字组成。[本文](https://whatismyipaddress.com/cidr)详细介绍了格式及其语法。

您可以在互联网上搜索免费的在线工具，这些工具将帮助您将现有的 IP 范围转换为 CIDR 格式。

## 最佳做法 {#best-practices}

在控制面板中将 IP 地址列入白名单时，请确保遵循以下建议和限制条件。

* **将 IP 范围列入白名单**，而非单个 IP 地址。要将单个 IP 地址列入白名单，请在其中附加“/32”，以标识该范围仅包含单个 IP 地址。
* **请勿将非常宽的范围列入白名单**，例如，包括超过 265 个 IP 地址的范围。控制面板将拒绝任何介于 /0 和 /23 之间的 CIDR 格式范围。
* 只能将&#x200B;**公共 IP 地址**&#x200B;列入白名单。
* 确保&#x200B;**定期删除您不再需要的已列入白名单的 IP 地址**。

## 将 IP 地址列入白名单 {#whitelisting-ip-addresses}

>[!CONTEXTUALHELP]
>id="cp_sftp_iprange_add"
>title="添加新 IP 范围"
>abstract="定义要列入白名单以连接到 SFTP 服务器的 IP 范围。"

要将 IP 范围列入白名单，请执行以下步骤：

1. 打开 **[!UICONTROL SFTP]**&#x200B;卡，然后选择 **[!UICONTROL IP Whistelisting]** 选项卡。
1. 将显示每个实例已列入白名单的 IP 地址列表。从左侧列表中选择所需的实例，然后单击 **[!UICONTROL Add new IP range]**&#x200B;按钮。

   ![](assets/control_panel_add_range.png)

1. 定义要列入白名单的 IP 范围（以 CIDR 格式），然后定义将在列表中显示的标签。

   >[!NOTE]
   >
   >标签字段中允许使用以下特殊字符：
   > `. _ - : / ( ) # , @ [ ] + = & ; { } ! $`

   ![](assets/control_panel_add_range2.png)

   >[!IMPORTANT]
   >
   >IP 范围不能与已列入白名单的现有范围重叠。在这种情况下，首先删除包含重叠 IP 的范围。
   >
   >可以将多个实例的范围列入白名单。为此，请按向下箭头键或键入所需实例的前几个字母，然后从建议列表中选择该实例。

   ![](assets/control_panel_add_range3.png)

1. 单击&#x200B;**[!UICONTROL Save]**&#x200B;按钮。在请求得到完全处理之前，IP 白名单添加项将显示为“待处理”。此处理操作只需要几秒钟即可完成。

要删除列入白名单的 IP 范围，请将其选中，然后单击 **[!UICONTROL Delete IP range]**&#x200B;按钮。

![](assets/control_panel_delete_range2.png)

>[!NOTE]
>
>当前无法编辑已列入白名单的范围。要修改 IP 范围，请将其删除，然后创建一个符合您的需求的 IP 范围。

## 监控更改 {#monitoring-changes}

通过控制面板主页中的 **[!UICONTROL Job Logs]**，您可以监控对列入白名单的 IP 地址所做的所有更改。

有关控制面板界面的详细信息，请参阅[此部分](../../discover/using/discovering-the-interface.md)。

![](assets/control_panel_ip_log.png)
