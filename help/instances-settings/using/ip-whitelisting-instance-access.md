---
title: 将 IP 列入白名单
description: 进一步了解在控制面板中将 IP 地址列入白名单以访问实例
translation-type: ht
source-git-commit: a2c19296894ff893987290cb287dc7002ab999e5
workflow-type: ht
source-wordcount: '705'
ht-degree: 100%

---


# 将 IP 列入白名单 {#ip-whitelisting}

>[!CONTEXTUALHELP]
>id="cp_instancesettings_iprange"
>title="关于将 IP 列入白名单"
>abstract="管理 IP 白名单以访问实例。"
>additional-url="https://images-tv.adobe.com/mpcv3/045cac99-f948-478e-ae04-f8c161dcb9e2_1568132508.1920x1080at3000_h264.mp4" text="观看演示视频"

>[!IMPORTANT]
>
>此功能仅适用于 Campaign Classic 实例。

## 关于将 IP 列入白名单 {#about-ip-whitelisting}

默认情况下，您的 Adobe Campaign Classic 实例无法从各种 IP 地址访问。

如果您的 IP 地址未列入白名单，您将无法从此地址登录到实例。同样，如果 IP 地址未明确与实例一起列入白名单，则您可能无法将 API 连接到消息中心或营销实例。

控制面板允许您通过将 IP 地址范围列入白名单来设置与实例的新连接。为此，请执行以下所述步骤：

将 IP 地址列入白名单后，您可以创建 Campaign 运算符并将其链接到它们，以便用户能够访问该实例。

## 最佳做法 {#best-practices}

在控制面板中将 IP 地址列入白名单时，请确保遵循以下建议和限制条件。

* **如果您不打算将 IP 地址连接到 RT 服务器**&#x200B;或 AEM 安全区域，请勿启用对所有访问类型的 IP 访问。
* **如果您临时启用了对 IP 地址实例的访问**，请确保在不再需要连接到实例时从已列入白名单的 IP 地址中删除 IP 地址。
* **我们不建议将公共场所**（机场、酒店等）的 IP 地址列入白名单。请始终使用公司 VPN 地址来保护实例的安全。

## 将 IP 地址列入白名单以进行实例访问 {#whistelisting-ip-addresses}

>[!CONTEXTUALHELP]
>id="cp_instancesettings_iprange_add"
>title="添加新 IP 范围"
>abstract="定义要列入白名单以连接到实例的 IP 范围。"

要将 IP 地址列入白名单，请执行以下步骤：

1. 打开 **[!UICONTROL Instances Settings card]**&#x200B;以访问 IP 白名单选项卡，然后单击 **[!UICONTROL Add new IP Range]**。

   >[!NOTE]
   >
   >如果“实例设置”卡未显示在控制面板的主页上，则表示您的 IMS ORG ID 未与任何 Adobe Campaign Classic 实例关联

   ![](assets/ip_whitelist_list1.png)

1. 按如下所述填写要列入白名单的 IP 范围信息。

   ![](assets/ip_whitelist_add1.png)

   * **[!UICONTROL Instance(s)]**：IP 地址能够连接的实例。可以同时处理多个实例。例如，可以通过同一步骤对生产实例和阶段实例将 IP 列入白名单。
   * **[!UICONTROL IP Range]**：要列入白名单的 IP 范围（以 CIDR 格式）。请注意，IP 范围不能与已列入白名单的现有范围重叠。在这种情况下，首先删除包含重叠 IP 的范围。
   >[!NOTE]
   >
   >CIDR（无类域间路由）是在控制面板界面中添加 IP 范围时受支持的格式。语法依次由 IP 地址、“/”字符和十进制数字组成。[本文](https://whatismyipaddress.com/cidr)详细介绍了格式及其语法。
   >
   >您可以在互联网上搜索免费的在线工具，这些工具将帮助您将现有的 IP 范围转换为 CIDR 格式。

   * **[!UICONTROL Label]**：将在已列入白名单的 IP 地址列表中显示的标签。
   * **[!UICONTROL Name]**：针对访问类型、实例（如果是外部 API 连接）和 IP 地址的名称必须是唯一的。


1. 指定要授予 IP 地址的访问类型：

   * **[!UICONTROL Campaign Console Access]**：允许 IP 地址连接到 Campaign Classic 控制台。请注意，仅对营销实例启用控制台访问。不允许访问 MID 和 RT 实例，因此不启用。
   * **[!UICONTROL AEM connection]**：允许指定的 AEM IP 地址连接到营销实例。
   * **[!UICONTROL External API connection]**：允许具有指定 IP 地址的外部 API 连接到营销和/或消息中心 (RT) 实例。请注意，未启用与 RT 实例控制台的连接。
   ![](assets/ip_whitelist_acesstype.png)

1. 单击&#x200B;**[!UICONTROL Save]**&#x200B;按钮。IP 范围将添加到已列入白名单的 IP 地址列表。

   ![](assets/ip_whitelist_added.png)

要删除列入白名单的 IP 范围，请将其选中，然后单击 **[!UICONTROL Delete IP range]**&#x200B;按钮。

**相关主题：**
* [将 IP 列入白名单（教程视频）](https://docs.adobe.com/content/help/en/campaign-learn/campaign-classic-tutorials/administrating/control-panel-acc/ip-whitelisting.html)
* [将安全区域链接到运算符](https://docs.campaign.adobe.com/doc/AC/en/INS_Additional_configurations_Configuring_Campaign_server.html#Linking_a_security_zone_to_an_operator)
