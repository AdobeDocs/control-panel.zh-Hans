---
product: campaign
solution: Campaign
title: 连接MID/RT实例
description: 了解如何将MID/RT实例连接到控制面板。
feature: Control Panel
role: Architect
level: Intermediate
source-git-commit: 1b712300bd7a1ef8dc784fa977f938bacc4c5e5b
workflow-type: tm+mt
source-wordcount: '284'
ht-degree: 2%

---


# 连接MID/RT实例

>[!CONTEXTUALHELP]
>id="cp_externalaccounts_url"
>title="子域详细信息"
>abstract="在此屏幕中，具有混合托管模型的客户可以提供其营销实例中存在的MID/RT实例，以便在控制面板中执行特定操作。"

控制面板允许具有混合托管模型的客户通过提供其营销实例中存在的MID/RT实例，在控制面板中执行特定操作。 有关托管模型的更多信息，请参阅 [Campaign Classic文档](https://experienceleague.adobe.com/docs/campaign-classic/using/installing-campaign-classic/architecture-and-hosting-models/hosting-models-lp/hosting-models.html).

## 连接MID/RT实例 {#connect}

>[!CONTEXTUALHELP]
>id="cp_externalaccounts_operator"
>title="子域详细信息"
>abstract="客户端控制台中用于在营销实例中添加MID/RT实例的运算符的ID。"

>[!CONTEXTUALHELP]
>id="cp_externalaccounts_password"
>title="子域详细信息"
>abstract="客户端控制台中用于在营销实例中添加MID/RT实例的运算符的密码。"

要在控制面板中提供MID/RT实例，请执行以下步骤：

1. 在 **[!UICONTROL Instances Settings]** 卡，选择 **[!UICONTROL External Accounts]** 选项卡。

1. 从下拉列表中选择营销实例，然后单击 **[!UICONTROL Add new URL]**.

   ![](assets/external-account-addbutton.png)

1. 提供有关要连接的MID/RT实例的信息：
   * **[!UICONTROL URL]**:实例的URL，
   * **[!UICONTROL Operator]** / **[!UICONTROL Password]**:客户端控制台中用于在营销实例中添加MID/RT实例的运算符的凭据。

   ![](assets/external-account-add.png)

1. 单击 **[!UICONTROL Save]** 确认。

您的实例现在已连接到控制面板。 您可以随时从列表中选择连接，以删除或停用该连接。

![](assets/external-account-edit.png)

## 可用于MID/RT实例的功能 {#capabilities}

将MID/RT实例连接到控制面板后，您可以利用下面列出的功能对其进行监控：

* [查看实例详细信息](../../instances-settings/using/instance-details.md),
* [向允许列表添加IP地址以访问实例](../../instances-settings/using/ip-allow-listing-instance-access.md),
* [查看有关委派的子域的信息](../../subdomains-certificates/using/setting-up-new-subdomain.md),
* [查看有关SSL证书的信息](../../subdomains-certificates/using/monitoring-ssl-certificates.md).
