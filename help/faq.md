---
title: 控制面板常见问题解答
description: 与控制面板相关的常见问题
translation-type: ht
source-git-commit: 35723590195ef54df42d1d1df5b37490787f8836
workflow-type: ht
source-wordcount: '629'
ht-degree: 100%

---


# 常见问题解答 {#faq}

## IMS 组织 ID {#ims-org-id}

**什么是 IMS 组织 ID？**

它是在您首次登录 Adobe Experience Cloud 时为您的实例提供的唯一 ID。其格式应为：xxx@AdobeOrg。

有关详细信息，请参阅 [Adobe Experience Cloud 文档](https://marketing.adobe.com/resources/help/zh_CN/mcloud/organizations.html)。

**在哪里可以找到我的 IMS 组织 ID？**

一种方法是导航到 [Adobe Experience Cloud 主页](https://experiencecloud.adobe.com/) >**[!UICONTROL Administration]**。您可在“管理”**[!UICONTROL Quick Access]**&#x200B;部分的底部找到您的 IMS 组织 ID。您可以在 [Adobe Experience Cloud 文档](https://marketing.adobe.com/resources/help/zh_CN/mcloud/organizations.html)中找到更多详细信息。

另一种方法是启动 **Admin Console**。您的 IMS 组织 ID 将显示在您的 URL 中，类似于：https://adminconsole.adobe.com/xxx@AdobeOrg/overview。

**为什么我需要知道我的 IMS 组织 ID？**

为了管理实例的设置，我们希望确保您获得正确实例的正确信息，在您的公司使用多个实例的情况下非常适用。

**如果我有多个 IMS 组织 ID，该怎么办？**

如果您有权访问多个 Adobe 解决方案，则您可拥有多个 IMS 组织 ID。在这种情况下，您应使用的正确 IMS 组织 ID 是您在 Adobe Campaign 实例下看到的 IMS 组织 ID。

>[!NOTE]
>
>如果您的 Adobe Campaign 和 Adobe Analytics 使用相同的 IMS 组织 ID，这是最好的。如果您计划集成解决方案以利用诸如放弃购物车（对于 AA + AC）等复杂的用例，则需要在 Analytics 和 Campaign 之间有一个 IMS 组织 ID。
>
>如果您的 Adobe Campaign 和 Adobe Analytics 有着不同的 IMS 组织 ID，请联系客服团队，以调整一致。

**如何确认我的 Adobe Campaign 实例是否托管在 AWS 上？**

要检查您的实例是否托管在 AWS 上，请执行以下步骤：

1. 检索您的登录 URL。它是您用于登录 Campaign 实例的 URL，通常以“.campaign.adobe.com”或“.neolane.net”结尾。
1. 打开终端，然后对您的登录 URL 执行 **[!DNL nslookup]**&#x200B;操作。

   `doe-macOS% nslookup myinstance.campaign.adobe.com`

1. 响应会返回有关实例的信息。

   ```
   doe-macOS% nslookup myinstance.campaign.adobe.com
   Server:     12.34.5.678
   Address:    12.34.5.678#99
   
   Non-authoritative answer:
   myinstance.campaign.adobe.com
   canonical name = myinstance-mkt-prod1.campaign.adobe.com.
   myinstance-mkt-prod1.campaign.adobe.com
   canonical name = myinstance-mkt-prod1-1.campaign.adobe.com.
   Name: myinstance-mkt-prod1-1.campaign.adobe.com
   Address: 12.34.567.89
   ```

1. 对返回的 IP 地址执行 **nslookup** 操作。

   `doe-macOS% nslookup 12.34.567.89`

1. 检查返回结果中的“name”值。如果它包含“amazonaws.com”，则表示您的实例托管在 AWS 上。

   ```
   doe-macOS% nslookup 12.34.567.89
   Server:     12.34.5.678
   Address:    12.34.5.678#99
   
   Non-authoritative answer:
   89.567.34.12.in-addr.arpa   name = ec2-12-34-567-89.address.amazonaws.com.
   ```

>[!NOTE]
>
>如果您希望迁移到 AWS，请联系您的客户成功经理开始该过程。

## 控制面板 {#control-panel}

**什么是控制面板？**

控制面板使产品管理员能够直接管理各种设置并监控连接到 Adobe Campaign 的 SFTP 服务器的容量。

**控制面板当前有哪些功能？**

通过控制面板，您可以根据自己的需求，跟踪存储、将 IP 添加到允许列表并管理 SFTP 服务器的 SSH 密钥和执行其他操作。

有关详细信息，请参阅控制面板支持的操作文档。

**控制面板是否仅用于 Adobe Campaign？**

是，您只能在控制面板中管理 Adobe Campaign 设置。

**我可以使用控制面板吗？**

控制面板仅对在 AWS 上托管 Adobe Campaign 的当前客户的产品管理员开放。请注意，尚不支持混合环境。

如果您不是管理员，但想要访问，请联系您的产品管理员将您添加为管理员。

**如何访问控制面板？**

请按照“访问控制面板”文档中的详细说明操作。

**使用控制面板是否需要额外付费？**

不需要，如果您当前是 Adobe Campaign 的客户，则不会产生额外费用。
