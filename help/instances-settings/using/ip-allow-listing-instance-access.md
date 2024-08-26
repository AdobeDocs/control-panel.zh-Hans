---
product: campaign
solution: Campaign
title: IP 允许列表
description: 了解如何在控制面板中向允许列表添加 IP 地址以进行实例访问
feature: Control Panel, Access Management
role: Admin
level: Intermediate
exl-id: 1d1eeff8-969e-4529-b947-2a68defb8d13
source-git-commit: a3485766791387bd9422b4f29daf86296efafb98
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# IP 允许列表 {#ip-allow-listing}

>[!CONTEXTUALHELP]
>id="cp_instancesettings_iprange"
>title="关于 IP 允许列表"
>abstract="向允许列表添加 IP 地址以进行访问实例。"
>additional-url="https://images-tv.adobe.com/mpcv3/045cac99-f948-478e-ae04-f8c161dcb9e2_1568132508.1920x1080at3000_h264.mp4" text="观看演示视频"

## 关于 IP 允许列表 {#about-ip-allow-listing}

>[!IMPORTANT]
>
>此功能仅适用于 Campaign v7/v8 实例。

默认情况下，无法从各种 IP 地址访问您的 Adobe Campaign 实例。

如果您的 IP 地址未添加到允许列表，您将无法从此地址登录到实例。同样，如果 IP 地址未明确与实例一起添加到允许列表，则您可能无法将 API 连接到消息中心或营销实例。

控制面板允许您通过将 IP 地址范围添加到允许列表来设置与实例的新连接。为此，请执行以下所述步骤：

将 IP 地址添加到允许列表后，您可以创建 Campaign 运算符并将其链接到它们，以便用户能够访问该实例。

![](assets/do-not-localize/how-to-video.png) [通过观看视频了解此功能](https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/instance-settings/ip-allow-listing.html?lang=zh-Hans#instance-settings)

## 最佳实践 {#best-practices}

在控制面板中将 IP 地址添加到允许列表时，请确保遵循以下建议和限制条件。

* **如果您不打算将 IP 地址连接到 RT 服务器**&#x200B;或 AEM 安全区域，请勿启用对所有访问类型的 IP 访问。
* **如果您临时启用了对 IP 地址实例的访问**，请确保在不再需要连接到实例时从允许列表中删除 IP 地址。
* **我们不建议将公共场所的 IP 地址添加到允许列表**（机场、酒店等）。请始终使用公司 VPN 地址来保护实例的安全。

## 将 IP 地址添加到允许列表以访问实例 {#adding-ip-addresses-allow-list}

>[!CONTEXTUALHELP]
>id="cp_instancesettings_iprange_add"
>title="IP 范围配置"
>abstract="定义要添加到允许列表以连接到实例的 IP 范围。"

>[!NOTE]
>
>如果&#x200B;**[!UICONTROL 实例设置]**&#x200B;信息卡未显示在控制面板的主页上，则表示您的[组织 ID](https://experienceleague.adobe.com/docs/core-services/interface/administration/organizations.html?lang=zh-Hans) 未与任何 Adobe Campaign v7/v8 实例关联。

要向允许列表添加 IP 地址，请执行以下步骤：

1. 打开&#x200B;**[!UICONTROL 实例设置信息卡]**&#x200B;以访问“IP 允许列表”选项卡，然后单击&#x200B;**[!UICONTROL 添加新 IP 范围]**。



   ![](assets/ip_whitelist_list1.png)

1. 按如下所述填写要添加到允许列表的 IP 范围信息。

   ![](assets/ip_whitelist_add1.png)

   * **[!UICONTROL 实例]**：IP 地址能够连接的实例。可以同时处理多个实例。例如，可以通过同一步骤对生产实例和阶段实例将 IP 添加到允许列表。
   * **[!UICONTROL IP 范围]**：要添加到允许列表的 IP 范围（CIDR 格式）。请注意，IP 范围不能与允许列表上的现有范围重叠。在这种情况下，首先删除包含重叠 IP 的范围。

   >[!NOTE]
   >
   >CIDR（无类域间路由）是在控制面板界面中添加 IP 范围时受支持的格式。语法依次由 IP 地址、“/”字符和十进制数字组成。[本文](https://whatismyipaddress.com/cidr)详细介绍了格式及其语法。
   >
   >您可以在互联网上搜索免费的在线工具，这些工具将帮助您将现有的 IP 范围转换为 CIDR 格式。

   * **[!UICONTROL 标签]**：将在允许列表中显示的标签。
   * **[!UICONTROL 名称]**：访问类型、实例（如果是外部 API 连接）和 IP 地址的名称必须是唯一的。

1. 指定要授予给 IP 地址的访问类型：

   * **[!UICONTROL Campaign 控制台访问]**：允许相应 IP 地址连接到 Campaign 客户端控制台。请注意，仅对营销实例启用控制台访问。不允许访问 MID 和 RT 实例，因此不启用。
   * **[!UICONTROL AEM 连接]**：允许指定的 AEM IP 地址连接到营销实例。
   * **[!UICONTROL 外部 API 连接]**：允许具有指定 IP 地址的外部 API 连接到营销和/或消息中心 (RT) 实例。请注意，未启用与 RT 实例控制台的连接。

   >[!NOTE]
   >
   >如果您使用具有混合托管模型的实例，则只能在“外部 API 连接”中为 MID 和 RT 实例添加 IP 地址。

   ![](assets/ip_whitelist_acesstype.png)

1. 单击&#x200B;**[!UICONTROL 保存]**&#x200B;按钮。IP 范围将被添加到允许列表。

   <!--![](assets/ip_whitelist_added.png)-->

默认情况下，无法从各种 IP 地址访问您的 Adobe Campaign 实例。

要从允许列表中删除一个或多个 IP 范围，请将其选中，然后单击&#x200B;**[!UICONTROL 删除 IP 范围]**&#x200B;按钮。

![](assets/ip_whitelist_delete.png)

**相关主题：**

* [将安全区域链接到运算符](https://experienceleague.adobe.com/docs/campaign-classic/using/installing-campaign-classic/additional-configurations/security-zones.html?lang=zh-Hans#linking-a-security-zone-to-an-operator)
