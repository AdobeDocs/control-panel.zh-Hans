---
title: 控制面板常见问题
description: 与控制面板相关的常见问题
translation-type: tm+mt
source-git-commit: 7bde86a86fbd128f4eb7bf029e58b0f95964390b
workflow-type: tm+mt
source-wordcount: '625'
ht-degree: 5%

---


# 常见问题解答 {#faq}

## IMS组织ID {#ims-org-id}

**什么是IMS组织ID?**

它是在您首次登录Adobe Experience Cloud时为您的实例提供的唯一ID。 它应采用以下格式： xxx@AdobeOrg。

有关详细信息，请参 [阅Adobe Experience Cloud文档](https://marketing.adobe.com/resources/help/zh_CN/mcloud/organizations.html)。

**在哪里可以找到我的IMS组织ID?**

One way is to navigate to [Adobe Experience Cloud Home](https://experiencecloud.adobe.com/) > **[!UICONTROL Administration]**. You will find your IMS Org ID at the bottom of Administration **[!UICONTROL Quick Access]** section. 您可以在 [Adobe Experience Cloud 文档](https://marketing.adobe.com/resources/help/zh_CN/mcloud/organizations.html)中找到更多详细信息。

另一种方法是启动 **Admin Console**。 您的IMS组织ID将显示在您的URL中，它应类似于： https://adminconsole.adobe.com/xxx@AdobeOrg/overview。

**为什么我需要了解我的IMS组织ID?**

为了便于您管理实例的设置，我们希望确保您获得正确实例的正确信息，以防您为公司使用多个实例。

**如果我有多个IMS组织ID怎么办？**

如果您有权访问多个Adobe解决方案，则您可能拥有多个IMS组织ID。 在这种情况下，您应使用的正确IMS组织ID是您在Adobe Campaign实例下看到的IMS组织ID。

>[!NOTE]
>
>如果您的Adobe Campaign和Adobe Analytics使用相同的IMS组织ID，那么这就太棒了。 如果您计划集成解决方案以利用诸如放弃购物车(AA + AC)等复杂的使用案例，则在Analytics和活动之间拥有一个IMS组织ID是一项要求。
>
>如果您有不同的IMS组织ID用于Adobe Campaign和Adobe Analytics，请联系客户服务部门，确保它们保持一致。

**我如何知道我的Adobe Campaign实例托管在AWS上？**

要检查您的实例是否托管在AWS上，请执行以下步骤：

1. 检索您的登录URL。 它是您用于登录活动实例的URL，其最后大部分以“.活动.adobe.com”或“.neolane.net”结尾。
1. 打开终端，然后对您 **[!DNL nslookup]** 的登录URL执行操作。

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

1. 对返回 **的** IP地址执行nslookup操作。

   `doe-macOS% nslookup 12.34.567.89`

1. 检查返回结果中的“name”值。 如果它包含“amazonaws.com”，则表示您的实例托管在AWS上。

   ```
   doe-macOS% nslookup 12.34.567.89
   Server:     12.34.5.678
   Address:    12.34.5.678#99
   
   Non-authoritative answer:
   89.567.34.12.in-addr.arpa   name = ec2-12-34-567-89.address.amazonaws.com.
   ```

>[!NOTE]
>
>如果您希望迁移到AWS，请联系您的客户成功经理来开始该过程。

## 控制面板 {#control-panel}

**什么是控制面板？**

控制面板使产品管理员能够直接管理各种设置并监控连接到Adobe Campaign的SFTP服务器的容量。

**控制面板当前有哪些功能？**

控制面板允许您根据自己的需要和其他操作，跟踪存储、白名单IP并管理SFTP服务器的SSH密钥。

有关详细信息，请参阅控制面板支持的操作文档。

**控制面板是否仅用于Adobe Campaign?**

是，您只能在控制面板中管理Adobe Campaign设置。

**是否可以使用控制面板？**

控制面板仅对在AWS上托管Adobe Campaign的当前客户的产品管理员开放。 请注意，尚不支持混合环境。

如果您不是管理员，但想要访问，请联系您的产品管理员以帮助您添加为管理员。

**如何访问控制面板？**

请按照访问控制面板文档中的详细说明操作。

**使用控制面板是否需要额外付费？**

不，如果您是当前的Adobe Campaign客户，则不会收取额外费用。
