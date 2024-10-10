---
product: campaign
solution: Campaign
title: 控制面板常见问题解答
description: 与控制面板相关的常见问题
feature: Control Panel
role: Admin
level: Intermediate
exl-id: 4f329764-ed8b-4939-affc-ed994fd6101d
source-git-commit: 98cf425548884c3a5e503c35ce5ea5b7ceaee67f
workflow-type: ht
source-wordcount: '719'
ht-degree: 100%

---

# 常见问题解答 {#faq}

## 控制面板 {#control-panel}

### 什么是控制面板？

通过控制面板，产品管理员能够直接管理各种设置并监测连接到 Adobe Campaign 的 SFTP 服务器的容量。

### 控制面板当前有哪些功能？

通过控制面板，您可以根据自己的需求，跟踪存储、将 IP 添加到允许列表并管理 SFTP 服务器的 SSH 密钥和执行其他操作。

有关详细信息，请参阅控制面板支持的操作文档。

### 是否有某些功能在 Campaign v8 上尚不支持，但在 Campaign Classic v7 上可用？{#v8-restrictions}

没有。现在，Campaign v8 控制面板支持 Campaign v7 的所有功能，包括子域和证书管理相关功能。

### 控制面板是否仅用于 Adobe Campaign？

是，您只能在控制面板中管理 Adobe Campaign 设置。

### 我可以使用控制面板吗？

控制面板仅对在 AWS 上托管 Adobe Campaign 的当前客户的产品管理员开放。

使用混合托管模型的客户可在控制面板中利用特定的控制面板功能。为此，他们需要在控制面板中提供其在营销实例中配置的 MID/RT 实例 URL。[了解详情](instances-settings/using/external-accounts.md)

如果您不是管理员，但想要访问，请联系您的产品管理员，让他们帮助将您添加为管理员。

### 作为 Campaign Classic v7 用户，访问控制面板需要什么条件？ {#v7-restrictions}

控制面板仅限管理员用户使用。[了解详情](discover/using/managing-permissions.md)。

请注意，Campaign v7 实例必须托管在 Amazon Web Services (AWS) 上，并升级到最新的 [Campaign 稳定版本](https://experienceleague.adobe.com/docs/campaign-classic/using/release-notes/rn-overview.html?lang=zh-Hans#rn-statuses)或 9032 版本及以上。请参阅[本节](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/starting-with-adobe-campaign/launching-adobe-campaign.html?lang=zh-Hans#getting-your-campaign-version)，了解如何查看 Campaign Classic v7 版本。要检查您的 Campaign Classic 实例是否托管在 AWS 上，请按照[本节](#hosted-aws)中详述的步骤操作。

### 如何访问控制面板？

请按照“访问控制面板”文档中的详细说明操作。

### 使用控制面板是否需要额外付费？

不需要，如果您当前是 Adobe Campaign 的客户，则不会产生额外费用。

## 组织 ID {#ims-org-id}

### 什么是组织 ID？

它是在您首次登录 Adobe Experience Cloud 时为您的实例提供的唯一 ID。其格式应为：xxx@AdobeOrg。

有关详细信息，请参阅 [Adobe Experience Cloud 文档](https://experienceleague.adobe.com/docs/core-services/interface/administration/organizations.html?lang=zh-Hans)。

### 在哪里可以找到我的组织 ID？

一种方法是导航到 [Adobe Experience Cloud 主页](https://experiencecloud.adobe.com/) > **[!UICONTROL 管理]**。您可在“管理”底部的&#x200B;**[!UICONTROL 快速访问]**&#x200B;部分中找到您的组织 ID。您可以在 [Adobe Experience Cloud 文档](https://experienceleague.adobe.com/docs/core-services/interface/administration/organizations.html?lang=zh-Hans)中找到更多详细信息。

另一种方法是启动 **Admin Console**。您的组织 ID 将显示在您的 URL 中，类似于：https://adminconsole.adobe.com/xxx@AdobeOrg/overview。

### 为什么我需要知道我的组织 ID？

为了管理实例的设置，我们希望确保您获得正确实例的正确信息，这在您的公司使用多个实例的情况下非常适用。

### 如果我有多个组织 ID，该怎么办？

如果您计划集成解决方案以利用复杂的用例，例如放弃购物车（适用于 Adobe Analytics + Adobe Campaign），则必须在 Analytics 和 Campaign 之间拥有组织 ID。如果您有权访问多个 Adobe 解决方案，则您可能会拥有多个组织 ID。在这种情况下，您应使用的正确组织 ID 是您在 Adobe Campaign 实例下看到的组织 ID。

<!--
>[!NOTE]
>
>If you have different organization IDs for Adobe Campaign and Adobe Analytics, please reach out to Customer Care to get them aligned.
-->

### 如何确认我的 Adobe Campaign 实例是否托管在 AWS 上？{#hosted-aws}

要检查您的实例是否托管在 AWS 上，请执行以下步骤：

1. 检索您的登录 URL。它是用于登录 Campaign 实例的 URL，通常以“.campaign.adobe.com”或“.neolane.net”结尾。
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
