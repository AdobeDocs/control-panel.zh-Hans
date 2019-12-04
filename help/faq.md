---
title: 控制面板常见问题解答
description: 与控制面板相关的常见问题
translation-type: tm+mt
source-git-commit: 8ee999b89af88a1a59956838d5722ce8fc6b3955

---


# 常见问题解答 {#faq}

## IMS组织ID {#ims-org-id}

**什么是IMS组织ID?**


它是在您首次登录Adobe Experience cloud时为您的实例提供的唯一ID。 它的格式应为：xxx@AdobeOrg。

有关详细信息，请参阅 [Adobe Experience cloud文档](https://marketing.adobe.com/resources/help/en_US/mcloud/organizations.html)。

**在哪里可以找到我的IMS组织ID?**

One way is to navigate to [Adobe Experience Cloud Home](https://exc-login.experiencecloud.adobe.com/exc-content/login.html?prefixtenantid=amc) &gt; **[!UICONTROL Administration]**. You will find your IMS Org ID at the bottom of Administration **[!UICONTROL Quick Access]** section. 您可以在 [Adobe Experience Cloud 文档](https://marketing.adobe.com/resources/help/en_US/mcloud/organizations.html)中找到更多详细信息。

另一种方法是启动 **Admin Console**。 您的IMS组织ID将显示在您的URL中，它应类似于：https://adminconsole.adobe.com/xxx@AdobeOrg/overview。

**为什么我需要了解我的IMS组织ID?**


为了便于您管理实例的设置，我们希望确保您获得了正确实例的正确信息，以防您为公司使用多个实例。

**如果我有多个IMS组织ID怎么办？**


如果您有权访问多个Adobe解决方案，则可能拥有多个IMS组织ID。 在这种情况下，您应使用的正确IMS组织ID是您在Adobe Campaign实例下看到的组织ID。

>[!NOTE]
>
>如果您拥有与Adobe Campaign和Adobe Analytics相同的IMS组织ID，那么这就太好了。 如果您计划集成解决方案以利用诸如购物车放弃（对于AA + AC）等复杂的使用案例，则在Analytics和Campaign之间拥有一个IMS组织ID是一项要求。
>
>如果您的Adobe Campaign和Adobe Analytics有不同的IMS组织ID，请联系客户关怀以使其保持一致。

**我如何知道我的Adobe Campaign实例是否托管在AWS上？**

要检查您的实例是否托管在AWS上，请执行以下步骤：

1. 检索您的登录URL。 它是您用来登录Campaign实例的URL，其最后大部分以“.campaign.adobe.com”结束。
1. 打开终端，然后对登录 **URL执行** nslookup操作。

   `doe-macOS% nslookup myinstance.campaign.adobe.com`

1. 响应会返回有关您的实例的信息。

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

1. 对返回 **的IP地址** ，执行nslookup操作。

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
>如果您希望迁移到AWS，请联系您的客户成功经理以开始该过程。

## 控制面板 {#control-panel}

**什么是控制面板？**


控制面板使产品管理员能够直接管理各种设置并监控连接到Adobe Campaign的SFTP服务器的容量。

**控制面板的当前功能有哪些？**


控制面板允许您根据自己的需求和其他操作来跟踪SFTP服务器的存储、白名单IP和管理SSH密钥。

有关详细信息，请参阅控制面板支持的操作文档。

**控制面板是否仅用于Adobe Campaign?**


是的，您只能在控制面板中管理Adobe Campaign的设置。

**我是否可以使用控制面板？**


控制面板仅对在AWS上托管Adobe Campaign的当前客户的产品管理员开放。

如果您不是管理员，但希望访问，请联系您的产品管理员以帮助您添加为管理员。

**如何访问控制面板？**

请按照访问控制面板文档中的详细说明操作。

**使用控制面板是否需要额外付费？**


否，如果您是Adobe Campaign的当前客户，则不会收取额外费用。
