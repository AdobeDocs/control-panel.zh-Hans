---
title: URL权限
description: 了解如何在控制面板中管理URL权限
translation-type: tm+mt
source-git-commit: f22e356b283ee2601c948d5c1d514a9a59c58451

---


# URL权限 {#url-permissions}

>[!CONTEXTUALHELP]
>id=&quot;cp_instancesettings_urlpermissions&quot;
>title=&quot;关于URL权限&quot;
>abstract=&quot;管理Adobe Campaign实例可以连接的URL。&quot;
>additional-url=&quot;https://images-tv.adobe.com/mpcv3/91206a19-d9af-4b6a-8197-0d2810a78941_1563488165.1920x1080at3000_h264.mp4&quot; text=&quot;观看演示视频&quot;

>[!CAUTION]
>
>此功能仅对Campaign Classic实例可用。

## 关于URL权限 {#about-url-permissions}

可由JavaScript代码（工作流等）调用的URL的默认列表活动经典实例的限制。 这些URL允许实例正常工作。

默认情况下，实例不允许连接到外部URL。 控制面板允许您将一些外部URL添加到授权URL列表，以便实例可以连接到它们。 这允许您将Campaign实例连接到外部系统（例如，SFTP服务器或网站），以启用文件和／或数据传输。

添加URL后，该URL将在实例的配置文件(serverConf.xml)中引用。

**相关主题：**

* [配置Campaign服务器](https://docs.campaign.adobe.com/doc/AC/en/INS_Additional_configurations_Configuring_Campaign_server.html)
* [输出连接保护](https://docs.campaign.adobe.com/doc/AC/en/INS_Additional_configurations_Configuring_Campaign_server.html#Outgoing_connection_protection)
* [添加URL权限（教程视频）](https://docs.adobe.com/content/help/en/campaign-learn/campaign-classic-tutorials/administrating/control-panel-acc/adding-url-permissions.html)

## 最佳实践 {#best-practices}

* 请勿将您的Campaign实例连接到您不想连接到的网站／服务器。
* 删除您不再使用的URL。 但是，请注意，如果您公司的其他部分仍连接到您删除的URL，则没有人会再次使用它。
* 控制面板支持 **http**、 **https**&#x200B;和 **sftp** 协议。 输入无效的URL或协议将导致错误。

## 管理URL权限 {#managing-url-permissions}

>[!CONTEXTUALHELP]
>id=&quot;cp_instancesettings_url_add&quot;
>title=&quot;添加新URL&quot;
>abstract=&quot;添加URL以允许与您的Campaign实例连接。&quot;

要添加实例可以连接到的URL，请执行以下步骤：

1. 打开卡 **[!UICONTROL Instances Settings]** 以访问选 **[!UICONTROL URL Permissions]** 项卡。

   >[!NOTE]
   >
   >如果“实例设置”卡未显示在控制面板的主页上，则表示您的IMS ORG ID未与任何Adobe Campaign Classic实例关联
   >
   >“ <b><span class="uicontrol">URL权限</span></b> ”选项卡列出了实例可以连接到的所有外部URL。 此列表不包括Campaign工作所需的URL（例如，基础结构部分之间的连接）。

1. 在左窗格中选择所需的实例，然后单击按 **[!UICONTROL Add new URL]** 钮。

   ![](assets/add_url1.png)

   >[!NOTE]
   >
   >您的所有营销活动实例都显示在左侧窗格列表中。
   >
   >由于URL权限管理仅专用于系列活动经典实例，因此，如果您选择了系列活动标准实例，则会显示“非适用实例”消息。

1. 键入要授权的URL及其关联协议（http、https或sftp）。

   >[!NOTE]
   >
   >可以授权多个实例连接到URL。 为此，请直接从“实例”字段中键入其第一个字母来添加它们。

   ![](assets/add_url2.png)

1. 该URL已添加到列表，您现在可以连接到它。

   >[!NOTE]
   >
   >“/.*”字符会自动添加到您在验证后输入的URL的末尾，以覆盖输入页面的所有子页面。

   ![](assets/add_url_listnew.png)

您可以随时删除URL，方法是选择该URL并单击该按 **[!UICONTROL Delete URL]** 钮。

请记住，如果删除URL，您的实例将无法再次调用它。

## 常见问题 {#common-questions}

**我添加了一个新URL，但我的实例仍无法连接到该URL。 为什么？**

在某些情况下，您尝试连接的URL需要白名单、密码输入或其他身份验证形式。 控制面板不管理其他身份验证。
