---
title: 实例详细信息
description: 了解如何在控制面板中监视实例详细信息
translation-type: tm+mt
source-git-commit: a2c19296894ff893987290cb287dc7002ab999e5

---


# 实例详细信息 {#instance-details}

>[!CONTEXTUALHELP]
>id=&quot;cp_instancesettings_instancedetails&quot;
>title=&quot;关于实例详细信息&quot;
>abstract=&quot;视图Adobe Campaign实例的详细信息：类型、名称、构建信息和可能的升级建议。”
>additional-url=&quot;https://docs.adobe.com/content/help/en/campaign-classic/using/release-notes/latest-release.html&quot; text=&quot;Campaign Classic发行说明&quot;
>additional-url=&quot;https://docs.adobe.com/content/help/en/campaign-standard/using/release-notes/release-notes.html&quot; text=&quot;Campaign Standard发行说明&quot;

>[!IMPORTANT]
>
>此功能仅对Campaign Classic实例可用。

## 关于实例详细信息 {#about-instance-details}

您的Adobe Campaign经典实例架构可以包含多台服务器，以实现营销活动的灵活性。 例如，您可以拥有营销、实时（或消息中心）和中间采购服务器来支持您的实例。

“实例详细信息”功能允许您视图实例的平面架构。 除了服务器信息外，它还会告知您实例构建是否是最新版本，并建议您在需要时进行升级。

>[!NOTE]
>
>我们建议您的实例每年至少升级一次，以避免性能下降，并能够利用Adobe Campaign经典必须优惠的最新功能和修复。

**相关主题：**

* [执行内部版本升级](https://docs.campaign.adobe.com/doc/AC/getting_started/EN/buildUpgrade.html)
* [更新Adobe Campaign](https://docs.campaign.adobe.com/doc/AC/en/PRO_Updating_Adobe_Campaign_Introduction.html)

## 检索有关实例的信息 {#retrieving-information-about-instances}

要获取有关连接到实例的服务器的信息，请执行以下步骤：

1. 打开卡 **[!UICONTROL Instances Settings]** 以访问选 **[!UICONTROL Instance Details]** 项卡。

   >[!NOTE]
   >
   >如果“实例设置”卡未显示在控制面板的主页上，则表明您的IMS ORG ID未与任何Adobe Campaign经典实例关联

1. 在左窗格中选择所需的Campaign Classic实例。

   >[!NOTE]
   >
   >您的所有活动实例都显示在左窗格列表中。 由于“实例详细信息”功能仅专用于Campaign Classic实例，因此，如果您选择了Campaign Standard实例，则会显示“非适用实例”消息。

1. 将显示连接到实例的服务器。

   ![](assets/instance_details.png)

可用信息包括：

* **[!UICONTROL Type]**:服务器的类型。 可能的值包括MKT（营销）、MID（中间采购）和RT（消息中心／实时消息）。
* **[!UICONTROL Name]**:服务器的名称。
* **[!UICONTROL Build:]** 服务器上安装的内部版本。
* **[!UICONTROL Upgrade info]**:此列将通知您是否需要服务器进行任何更新。
   * 绿色：您的服务器是最新的，无需升级。
   * 黄色：您应该考虑升级。 您缺少最新的功能和修复。
   * 红色：尽快升级。 您缺少新功能，服务器性能可能不是最佳的。

如果您的某台服务器需要升级，请参阅 [本文档](https://docs.campaign.adobe.com/doc/AC/getting_started/EN/buildUpgrade.html) ，了解有关如何继续的详细信息。

## 常见问题 {#common-questions}

**我在实例架构上看不到MID服务器，是否表示我的实例无法正常运行？ 我是否需要RT实例才能做到今天做不到的事？**

您自己的实例看起来可能会非常不同，它可能并不具有所有类型的服务器，也可能具有多个相同的服务器。 没有一种或另一种类型的服务器并不意味着您无法发送实时消息或执行其他类型的活动。 您可以请求额外的服务器容量，并收取额外费用。

如果您认为某些服务器未显示在“实例详细信息”页面，请联系客户关怀。 确保在消息中记下特定实例URL。
