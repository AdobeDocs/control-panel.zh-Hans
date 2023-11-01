---
product: campaign
solution: Campaign
title: 将 IP 范围添加到允许列表
description: 了解如何将 IP 范围添加到 SFTP 服务器访问允许列表
feature: Control Panel, SFTP Management
role: Admin
level: Experienced
exl-id: 45a3bfcd-500c-4139-b610-d39989260ab7
source-git-commit: a3485766791387bd9422b4f29daf86296efafb98
workflow-type: tm+mt
source-wordcount: '1080'
ht-degree: 35%

---

# 将 IP 范围添加到允许列表 {#ip-range-allow-listing}

>[!CONTEXTUALHELP]
>id="cp_ip_whitelist"
>title="关于 IP 允许列表"
>abstract="在此选项卡中，您可以向允许列表添加 IP 范围，以建立与 SFTP 服务器的连接。此处仅显示您有权访问的 SFTP 服务器。请联系您的管理员以请求访问其他 SFTP 服务器。"
>additional-url="https://images-tv.adobe.com/mpcv3/8a977e03-d76c-44d3-853c-95d0b799c870_1560205338.1920x1080at3000_h264.mp4#t=98" text="观看演示视频"

SFTP 服务器受到保护。为了能够访问这些服务器以查看文件或编写新文件，您需要将访问服务器的系统或客户端的公共IP地址添加到允许列表中。

![](assets/do-not-localize/how-to-video.png)在使用 [Campaign v7/v8](https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/sftp-management/adding-ip-range-to-allow-list.html#sftp-management) 或 [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/sftp-management/adding-ip-range-to-allow-list.html#sftp-management) 的视频中了解这一功能

## 关于 CIDR 格式 {#about-cidr-format}

CIDR（无类域间路由）是在控制面板界面中添加 IP 范围时受支持的格式。

语法依次由 IP 地址、“/”字符和十进制数字组成。有关格式及其语法的详情，请参阅 [本文](https://whatismyipaddress.com/cidr){target="_blank"}.

您可以在Internet上搜索免费的在线工具，这些工具将帮助您将现有的IP范围转换为CIDR格式。

## 最佳实践 {#best-practices}

在控制面板中将 IP 地址添加到允许列表时，请确保遵循以下建议和限制条件。

* **将 IP 范围添加到允许列表**，而不是单个 IP 地址。要将单个 IP 地址添加到允许列表，请在其中附加“/32”，以标识该范围仅包含单个 IP 地址。
* **请勿向允许列表添加非常宽的范围**，例如，包括 > 265 个 IP 地址。控制面板将拒绝任何介于 /0 和 /23 之间的 CIDR 格式范围。
* 只能将&#x200B;**公共 IP 地址**&#x200B;添加到允许列表。
* 确保 **定期删除IP地址** 你不再需要从允许列表中获取这些信息。

## 向允许列表添加 IP 地址 {#adding-ip-addresses-allow-list}

>[!CONTEXTUALHELP]
>id="cp_sftp_iprange_add"
>title="IP 范围配置"
>abstract="定义要添加到允许列表以连接到 SFTP 服务器的 IP 范围。"

要向允许列表添加 IP 范围，请执行以下步骤：

1. 打开 **[!UICONTROL SFTP]** 信息卡，然后选择 **[!UICONTROL IP允许列表]** 选项卡。
1. 将为每个实例显示允许列表上的 IP 地址列表。从左侧列表中选择所需的实例，然后单击 **[!UICONTROL 添加新IP范围]** 按钮。

   ![](assets/control_panel_add_range.png)

1. 定义要添加到允许列表的IP范围。 此字段仅接受CIDR格式的IP范围，例如 *192.150.5.0/24*.

   ![](assets/control_panel_add_range4.png)

   >[!IMPORTANT]
   >
   >IP 范围不能与允许列表上的现有范围重叠。在这种情况下，首先删除包含重叠 IP 的范围。

1. 可以为多个实例向允许列表添加一个范围。 为此，请按向下箭头键或键入所需实例的前几个字母，然后从建议列表中选择该实例。

   ![](assets/control_panel_add_range3.png)

1. 定义将在列表中为此IP范围显示的标签。

   ![](assets/control_panel_add_range2.png)

   >[!NOTE]
   >
   >中允许使用以下特殊字符 **[!UICONTROL 标签]** 字段：
   > `. _ - : / ( ) # , @ [ ] + = & ; { } ! $`

1. 为了更好地管理IP允许列表，您可以设置每个IP范围可用性的持续时间。 要执行此操作，请在 **[!UICONTROL 类型]** 下拉列表，并在相应的字段中定义持续时间。 有关IP范围到期的详细信息，请参阅 [本节](#expiry).

   ![](assets/control_panel_add_range5.png)

   >[!NOTE]
   >
   >默认情况下， **[!UICONTROL 类型]** 字段设置为 **[!UICONTROL 无限制]**，这意味着IP范围永不过期。

1. 在 **[!UICONTROL 注释]** 字段中，您可以指示允许此IP范围的原因（原因、对象等）。

1. 单击 **[!UICONTROL 保存]** 按钮。 允许列表的IP范围添加项将显示为 **[!UICONTROL 待处理]** 直到完全处理请求，这应该只需要几秒钟。

   ![](assets/control_panel_add_range6.png)

>[!IMPORTANT]
>
>如果您尝试将SFTP服务器连接到新系统，从而向允许列表添加新的IP范围，则可能需要输入新的公钥以完成连接。 有关更多信息，请参阅[此章节](key-management.md)。

## 管理IP范围 {#managing-ip-ranges}

您创建的IP范围将显示在 **[!UICONTROL IP允许列表]** 选项卡。

您可以根据创建日期或编辑日期、创建或编辑项目的用户以及IP范围到期对项目进行排序。

您还可以通过开始键入标签、范围、名称或注释来搜索IP范围。

![](assets/control_panel_allow_list_sort.png)

要编辑一个或多个IP范围，请参阅 [本节](#editing-ip-ranges).

要从允许列表中删除一个或多个IP范围，请选择它们，然后单击 **[!UICONTROL 删除IP范围]** 按钮。

![](assets/control_panel_delete_range.png)

### 到期 {#expiry}

此 **[!UICONTROL 过期]** 列显示了IP范围过期前的剩余天数。

如果您订阅了 [电子邮件警报](../../performance-monitoring/using/email-alerting.md)，您将在IP范围过期的10天和5天前以及过期日期当天通过电子邮件收到通知。 收到警报后，您可以 [编辑IP范围](#editing-ip-ranges) 以根据需要延长有效期。

过期的IP范围将在7天后自动删除。 它显示为 **[!UICONTROL 已过期]** 在 **[!UICONTROL 过期]** 列。 在这7天内：

* 已过期的IP范围无法再用于访问SFTP服务器。

* 无法创建与过期范围重叠的另一个IP范围。 您需要先删除过期的IP范围，然后再创建新范围。

* 您可以 [编辑](#editing-ip-ranges) 过期的IP范围并更新其持续时间，以使其再次可用。

* 您可以将其从允许列表中删除。

## 编辑IP范围 {#editing-ip-ranges}

>[!CONTEXTUALHELP]
>id="cp_sftp_iprange_update"
>title="更新 IP 范围"
>abstract="更新允许连接到 SFTP 服务器的选定 IP 范围。"

要编辑IP范围，请执行以下步骤。

>[!NOTE]
>
>您只能编辑自2021年10月发布控制面板以来创建的IP范围。

<!--Edition is not available for IP ranges that have been created before the Control Panel October 2021 release.-->

1. 从中选择一个或多个IP范围 **[!UICONTROL IP允许列表]** 列表。

1. 单击 **[!UICONTROL 更新IP范围]** 按钮。

   ![](assets/control_panel_edit_range.png)

1. 您只能编辑IP范围到期和/或添加新注释。

   >[!NOTE]
   >
   >要修改CIDR格式、其标签或编辑相关实例，必须先删除IP范围，并根据需要创建新范围。

   ![](assets/control_panel_edit_range2.png)

1. 保存您的更改。

## 监控更改 {#monitoring-changes}

此 **[!UICONTROL 作业日志]** 通过控制面板主页中的，您可以跟踪和监控对允许列表上的IP地址所做的所有更改。

有关控制面板界面的详细信息，请参阅[此部分](../../discover/using/discovering-the-interface.md)。

![](assets/control_panel_ip_log.png)
