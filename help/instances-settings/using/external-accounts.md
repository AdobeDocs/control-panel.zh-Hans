---
product: campaign
solution: Campaign
title: 添加MID/RT实例（混合模型）
description: 了解如何添加MID/RT实例以控制面板混合托管模型。
feature: Control Panel
role: Architect
level: Intermediate
source-git-commit: 2458263ef5981a16d983912b498e320501df7889
workflow-type: tm+mt
source-wordcount: '461'
ht-degree: 3%

---


# 添加MID/RT实例（混合模型）

>[!CONTEXTUALHELP]
>id="cp_externalaccounts"
>title="外部帐户"
>abstract="在此屏幕中，具有混合托管模型的控制面板可以提供其在营销实例中配置的MID/RT实例URL，以便利用控制面板功能。"

控制面板允许具有混合托管模型的客户利用特定的控制面板功能。 为此，他们需要提供在其控制面板实例中配置的MID/RT实例URL。

有关托管模型的更多信息，请参阅 [Campaign Classic文档](https://experienceleague.adobe.com/docs/campaign-classic/using/installing-campaign-classic/architecture-and-hosting-models/hosting-models-lp/hosting-models.html).

## 添加MID/RT实例 {#add}

>[!CONTEXTUALHELP]
>id="cp_externalaccounts_url"
>title="URL"
>abstract="实例的URL，可在Campaign客户端控制台中的“管理”>“平台”>“外部帐户”菜单中找到。"

>[!CONTEXTUALHELP]
>id="cp_externalaccounts_operator"
>title="运算符"
>abstract="在由Adobe管理员初始配置后提供的运算符的ID。"

>[!CONTEXTUALHELP]
>id="cp_externalaccounts_password"
>title="密码"
>abstract="操作员在Adobe管理员初始配置后提供的密码。"

混合型客户应通过Experience Cloud连接到控制面板。 首次访问控制面板时，主页上仅显示两张卡片。

![](assets/hybrid-homepage.png)

>[!NOTE]
>
>如果您在访问控制面板时遇到任何问题，则很可能您的营销实例尚未映射到您的组织ID。 请联系客户关怀团队以完成此设置，以继续进一步操作。 成功连接后，您会看到控制面板主页。

要访问控制面板功能，您需要在 **[!UICONTROL Instances Settings]** 卡。 为此，请执行以下步骤：

1. 在 **[!UICONTROL Instances Settings]** 卡，选择 **[!UICONTROL External Accounts]** 选项卡。

1. 从下拉列表中选择所需的营销实例，然后单击 **[!UICONTROL Add new URL]**.

   ![](assets/external-account-addbutton.png)

1. 提供有关要添加的MID/RT实例的信息。

   ![](assets/external-account-add.png)

   * **[!UICONTROL URL]**:实例的URL，可在的Campaign客户端控制台(位于 **[!UICONTROL Administration]** > **[!UICONTROL Platform]** > **[!UICONTROL External Accounts]** 菜单。

      ![](assets/external-account-url.png)

   * **[!UICONTROL Operator]** / **[!UICONTROL Password]**:操作员在Adobe管理员初始配置后提供的凭据。

      >[!NOTE]
      >
      >如果这些详细信息不可用，请联系客户关怀团队。

1. 单击 **[!UICONTROL Save]** 确认。

添加MID/RT URL时，会触发异步进程以验证URL的正确性。 此过程可能需要几分钟时间。 在验证MID/RT实例URL之前，作业将处于待处理状态。 仅在验证完成时，您才能访问控制面板主要功能。

![](assets/external-account-pending.png)

您可以随时从列表中选择MID/RT实例URL，以将其删除或停用。

![](assets/external-account-edit.png)

请注意，您可以监控 **[!UICONTROL External Accounts]** 选项卡 **[!UICONTROL Job Logs]**:

![](assets/external-account-logs.png)

## 适用于混合客户的功能 {#capabilities}

将MID/RT实例添加到控制面板后，您可以利用下面列出的功能：

* [监测关键联系人和事件](../../service-events/service-events.md)
* [查看实例详细信息](../../instances-settings/using/instance-details.md),
* [向允许列表添加IP地址](../../instances-settings/using/ip-allow-listing-instance-access.md) （对于RT实例）、
* [查看有关委派的子域的信息](../../subdomains-certificates/using/monitoring-subdomains.md),
* [查看有关SSL证书的信息](../../subdomains-certificates/using/monitoring-ssl-certificates.md).