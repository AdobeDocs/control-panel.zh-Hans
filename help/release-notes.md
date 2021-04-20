---
product: campaign
solution: Campaign
title: 控制面板版本
description: 最新控制面板发行说明。
feature: Control Panel
role: Architect
level: Beginner
exl-id: 13aceffb-ceaa-4cfe-8741-95d66c5c6caa
translation-type: tm+mt
source-git-commit: 4c8347f7b0f4a776ea726f02029ea1c92a83406a
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# 控制面板版本 {#control-panel-releases}

您将在此处找到有关最新控制面板版本的信息。

>[!NOTE]
>
>所有管理员用户都可访问控制面板。[此部分](https://experienceleague.adobe.com/docs/control-panel/using/discover-control-panel/managing-permissions.html?lang=zh-Hans#discover-control-panel)将详细介绍授予用户管理员访问权限的步骤。
>
>对于 Campaign Classic，请注意，您的实例必须托管在 AWS 上，并使用最新的 [Gold Standard](https://experienceleague.adobe.com/docs/campaign-classic/using/release-notes/gs-release/gs-overview.html?lang=zh-Hans) 版本或最新的[ GA 版本 (21.1)](https://experienceleague.adobe.com/docs/campaign-classic/using/release-notes/latest-release.html?lang=zh-Hans#release-notes) 进行升级。在[本节](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/starting-with-adobe-campaign/launching-adobe-campaign.html?lang=zh-Hans#getting-your-campaign-version)中了解如何确认您的版本。要检查您的实例是否托管在 AWS 上，请按照[此页面](faq.md)中详述的步骤操作。

## 2020 年 10 月 {#october-2020}

**使用 CNAME 的子域配置**

控制面板现在可让您配置子域以直接从界面使用 CNAME 处理 Adobe。[阅读更多](subdomains-certificates/using/setting-up-new-subdomain.md)

**数据库监视增强功能**

数据库监视功能已得到增强，增加了一些指标，使您能够获得有关占用数据库空间的资源的详细信息。 [阅读更多](performance-monitoring/using/database-monitoring.md)

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
