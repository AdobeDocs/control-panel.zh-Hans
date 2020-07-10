---
title: IP允许列表
description: 了解如何在控制面板中向允许列表添加IP地址以进行实例访问
translation-type: tm+mt
source-git-commit: 35723590195ef54df42d1d1df5b37490787f8836
workflow-type: tm+mt
source-wordcount: '765'
ht-degree: 45%

---


# IP允许列表 {#ip-allow-listing}

>[!CONTEXTUALHELP]
>id="cp_instancesettings_iprange"
>title="关于IP允许列表"
>abstract="向允许列表添加IP地址以访问实例。"
>additional-url="https://images-tv.adobe.com/mpcv3/045cac99-f948-478e-ae04-f8c161dcb9e2_1568132508.1920x1080at3000_h264.mp4" text="观看演示视频"

>[!IMPORTANT]
>
>此功能仅适用于 Campaign Classic 实例。

## 关于IP允许列表 {#about-ip-allow-listing}

默认情况下，您的 Adobe Campaign Classic 实例无法从各种 IP 地址访问。

如果您的IP地址尚未添加到允许列表，您将无法从此地址登录到实例。 同样，如果IP地址尚未与实例明确添加到允许列表，您可能无法将API连接到消息中心或营销实例。

控制面板允许您通过向允许列表添加IP地址范围来设置到实例的新连接。 为此，请执行以下所述步骤：

IP地址在允许列表上后，您可以创建活动运算符并将其链接到这些运算符，以便用户能够访问该实例。

## 最佳做法 {#best-practices}

确保在控制面板中向允许列表添加IP地址时遵循以下建议和限制。

* **如果您不打算将 IP 地址连接到 RT 服务器**&#x200B;或 AEM 安全区域，请勿启用对所有访问类型的 IP 访问。
* **如果为某个IP地址暂时启用了对实例的访问**，请确保在不再需要连接到实例时从允许列表中删除IP地址。
* **我们不建议向允许列表(机场、酒店等** )添加公共场所的IP地址。 请始终使用公司 VPN 地址来保护实例的安全。

## 将IP地址添加到实例访问允许列表 {#adding-ip-addresses-allow-list}

>[!CONTEXTUALHELP]
>id="cp_instancesettings_iprange_add"
>title="添加新 IP 范围"
>abstract="定义要添加到允许列表以连接到实例的IP范围。"

要向允许列表添加IP地址，请执行以下步骤：

1. Open the **[!UICONTROL Instances Settings card]** to access the IP allow listing tab, then click **[!UICONTROL Add new IP Range]**.

   >[!NOTE]
   >
   >如果“Control Panel（控制面板）”主页上未显示“Instance Settings（实例设置）”卡，则表示您的IMS组织ID未与任何Adobe Campaign经典实例关联

   ![](assets/ip_whitelist_list1.png)

1. 按如下所述填写要添加到允许列表的IP范围信息。

   ![](assets/ip_whitelist_add1.png)

   * **[!UICONTROL Instance(s)]**：IP 地址能够连接的实例。可以同时处理多个实例。例如，可以通过同一步骤对生产实例和舞台实例执行IP允许列表。
   * **[!UICONTROL IP Range]**: 要添加到允许列表的IP范围，CIDR格式。 请注意，IP范围不能与允许列表上的现有范围重叠。 在这种情况下，首先删除包含重叠 IP 的范围。

   >[!NOTE]
   >
   >CIDR（无类域间路由）是在控制面板界面中添加 IP 范围时受支持的格式。语法依次由 IP 地址、“/”字符和十进制数字组成。[本文](https://whatismyipaddress.com/cidr)详细介绍了格式及其语法。
   >
   >您可以在互联网上搜索免费的在线工具，这些工具将帮助您将现有的 IP 范围转换为 CIDR 格式。

   * **[!UICONTROL Label]**: 将在允许列表中显示的标签。
   * **[!UICONTROL Name]**：针对访问类型、实例（如果是外部 API 连接）和 IP 地址的名称必须是唯一的。


1. 指定要授予 IP 地址的访问类型：

   * **[!UICONTROL Campaign Console Access]**：允许 IP 地址连接到 Campaign Classic 控制台。请注意，仅对营销实例启用控制台访问。不允许访问 MID 和 RT 实例，因此不启用。
   * **[!UICONTROL AEM connection]**：允许指定的 AEM IP 地址连接到营销实例。
   * **[!UICONTROL External API connection]**：允许具有指定 IP 地址的外部 API 连接到营销和/或消息中心 (RT) 实例。请注意，未启用与 RT 实例控制台的连接。

   ![](assets/ip_whitelist_acesstype.png)

1. 单击&#x200B;**[!UICONTROL Save]**&#x200B;按钮。IP范围将添加到允许列表。

   ![](assets/ip_whitelist_added.png)

要从允许列表中删除IP范围，请选择它们，然后单击 **[!UICONTROL Delete IP range]** 按钮。

**相关主题：**
* [IP允许列表（教程视频）](https://docs.adobe.com/content/help/en/campaign-learn/campaign-classic-tutorials/administrating/control-panel-acc/ip-allow-listing.html)
* [将安全区域链接到运算符](https://docs.campaign.adobe.com/doc/AC/en/INS_Additional_configurations_Configuring_Campaign_server.html#Linking_a_security_zone_to_an_operator)
