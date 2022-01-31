---
product: campaign
solution: Campaign
title: 控制面板版本
description: 最新控制面板发行说明。
feature: Control Panel
role: Architect
level: Beginner
exl-id: 13aceffb-ceaa-4cfe-8741-95d66c5c6caa
source-git-commit: 10c4cf41dc9502bb66566951780cf8f963b08aa9
workflow-type: tm+mt
source-wordcount: '858'
ht-degree: 65%

---

# 控制面板版本 {#control-panel-releases}

您将在此处找到有关最新控制面板版本的信息。

>[!NOTE]
>
>控制面板仅供管理员用户访问。 了解有关 [此部分](https://experienceleague.adobe.com/docs/control-panel/using/discover-control-panel/managing-permissions.html?lang=zh-Hans#discover-control-panel).
>
>对于Campaign Classicv7，您的实例必须托管在Amazon Web Services(AWS)上并升级到最新版本 [营销活动稳定内部版本](https://experienceleague.adobe.com/docs/campaign-classic/using/release-notes/rn-overview.html?lang=zh-Hans#rn-statuses) （或构建9032或更高版本）。 在[本节](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/starting-with-adobe-campaign/launching-adobe-campaign.html?lang=zh-Hans#getting-your-campaign-version)中了解如何确认您的版本。要检查您的实例是否托管在 AWS 上，请按照[此页面](faq.md#hosted-aws)中详述的步骤操作。

## 2022 年 1 月 {#january-2022}

**活动查询监控**

控制面板现在允许您监视在实例上运行时间最长的查询。 [了解更多信息](performance-monitoring/using/database-active-queries.md)

**吞吐量和延迟监控**

您现在可以监控在实例上一段时间内的投放吞吐量和延迟趋势。 [了解更多信息](performance-monitoring/using/thoughputs-latencies.md)

**对新子域执行SSL证书操作**

现在，即使可交付性审核仍在进行中，也可以对新设置的子域执行SSL证书操作。 [了解更多信息](subdomains-certificates/using/renewing-subdomain-certificate.md)

## 2021 年 10 月 {#october-2021}

**IP范围和公钥有效期**

现在，可以设置IP范围和公共密钥可用性的持续时间。 有关更多信息，请参阅 [IP范围允许列表](sftp/using/ip-range-allow-listing.md#adding-ip-addresses-allow-list) 和 [密钥管理](sftp/using/key-management.md#installing-ssh-key) 中。

**IP范围和公钥版本**

您现在可以编辑 [IP范围](sftp/using/ip-range-allow-listing.md#editing-ip-ranges) 和 [公共密钥](sftp/using/key-management.md#editing-public-keys) 创建的。 请注意，此功能不适用于在当前控制面板版本之前创建的项目。

**SFTP IP范围和公钥到期警报**

电子邮件警报功能现在包含有关SFTP IP允许列表过期和SFTP公钥过期的警报。 [了解更多信息](performance-monitoring/using/email-alerting.md)

**Campaign v8 提供全面支持**

的 **子域** 和 **证书** Adobe Campaign v8上的控制面板现在支持管理功能。

## 2021 年 8 月 {#august-2021}

**支持Campaign v8**

控制面板现在可用于Adobe Campaign v8，但 **子域** 和 **证书** 管理功能，但尚不受支持。 在 [Campaign v8文档](https://experienceleague.adobe.com/docs/campaign/campaign-v8/deploy/self-service.html){target=&quot;_blank&quot;}

## 2020 年 10 月 {#october-2020}

**使用 CNAME 的子域配置**

控制面板现在可让您配置子域以直接从界面使用 CNAME 处理 Adobe。[阅读更多](subdomains-certificates/using/setting-up-new-subdomain.md)

**数据库监视增强功能**

数据库监控已通过其他量度得到增强，这些量度允许您获取有关占用数据库空间的资源的详细信息。 [阅读更多](performance-monitoring/using/database-monitoring.md)

## 2020 年 6 月 {#june-2020}

**子域可交付性审核**

委派新子域后，控制面板现在允许您跟踪可交付性团队执行的审核。[阅读更多](subdomains-certificates/using/setting-up-new-subdomain.md)

**GPG 密钥管理**

现在，控制面板允许您生成一对 GPG 密钥，以便您可以从外部轻松解密进入 Campaign 的数据。此外，我们还添加了一项功能，以便您可以安装公共 GPG 密钥来加密离开 Campaign 的数据。[阅读更多](instances-settings/using/gpg-keys-management.md)

**活动用户档案监控**

控制面板现在允许您监控实例使用的活动用户档案数，并计数用于计费目的。[阅读更多](performance-monitoring/using/active-profiles-monitoring.md)

>[!IMPORTANT]
>
>测试版中提供控制面板的活动用户档案监控，如有频繁更新和修改，恕不另行通知。

## 2020 年 5 月 {#may-2020}

**CNAME 子域的证书管理**

控制面板现在可让您续订已使用 CNAME 方式配置的子域的 SSL 证书。[阅读更多](subdomains-certificates/using/renewing-subdomain-certificate.md)

## 2020 年 4 月 {#april-2020}

**Google TXT 记录管理**

将 Google TXT 网站验证记录添加到所有子域，这些子域用于通过 Campaign 控制面板向 Gmail 地址发送电子邮件。[阅读更多](subdomains-certificates/using/managing-txt-records.md)

**数据库空间监控**

Campaign 控制面板配备了数据库监控功能，允许您查看按需数据库空间利用率以及随时间推移的利用率。[阅读更多](performance-monitoring/using/database-monitoring.md)

**电子邮件警报**

Campaign 控制面板具备实时电子邮件警报功能，您可以登录控制面板并注册，以在系统面临性能下降风险时接收警报，或者需要采取措施以确保未来的高性能时接收警报。[阅读更多](performance-monitoring/using/email-alerting.md)

## 2020 年 1 月 {#january-2020}

*2020 年 1 月 22 日*

我们为管理员用户添加了新功能，以便从控制面板配置子域和续订 SSL 证书。

有关详细信息，请参阅以下页面：
* [设置新子域](subdomains-certificates/using/setting-up-new-subdomain.md)
* [续订子域的 SSL 证书](subdomains-certificates/using/renewing-subdomain-certificate.md)

>[!IMPORTANT]
>
>这些功能将在测试版中提供，如有频繁更新和修改，恕不另行通知。

## 2019 年 9 月 {#september-2019}

*2019 年 9 月 16 日*

我们为管理员用户添加了新功能，以向允许列表添加 IP 地址，以便连接到 Campaign Classic 实例。
此外，管理员用户现在可以查看 Campaign Classic 实例的列表和具有版本升级资格。

有关详细信息，请参阅[专用文档](instances-settings/using/ip-allow-listing-instance-access.md)。

## 2019 年 8 月 {#august-2019}

我们添加了新功能，使管理员用户在域的 SSL 证书过期前接收通知。有关详细信息，请参阅[详细文档](subdomains-certificates/using/monitoring-ssl-certificates.md)。

此外，管理员用户现在可以删除为访问 SFTP 服务器而添加的 SSH 密钥。

## 2019 年 7 月 {#july-2019}

我们添加了新功能，使管理员用户能够更好地控制 Campaign Classic 实例设置。新的控制面板功能包括添加 Adobe Campaign 连接到的 URL 以进行数据/文件传输。

有关详细信息，请参阅[详细文档](instances-settings/using/url-permissions.md)。
