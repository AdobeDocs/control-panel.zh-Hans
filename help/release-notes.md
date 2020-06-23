---
title: 控制面板版本
translation-type: tm+mt
source-git-commit: 5b7e8126789690662e72e72c885700b971362004
workflow-type: tm+mt
source-wordcount: '577'
ht-degree: 70%

---


# 控制面板版本 {#control-panel-releases}

您将在此处找到有关控制面板版本的最新信息。

>[!NOTE]
>
>请注意，控制面板仅供托管在 AWS 上的客户使用，但尚不受支持的混合环境除外。访问控制面板无需升级。请确保您是管理员用户，才可以访问它。

## 2020年6月 {#june-2020}

**子域交付性审核**

委派新子域后，控制面板现在允许您跟踪可交付性团队执行的审核。 [阅读更多](subdomains-certificates/using/setting-up-new-subdomain.md)

**GPG 密钥管理**

现在，控制面板允许您生成一对 GPG 密钥，以便您可以从外部轻松解密进入 Campaign 的数据。此外，我们还添加了一项功能，以便您可以安装公共 GPG 密钥来加密离开 Campaign 的数据。[阅读更多](instances-settings/using/gpg-keys-management.md)

**删除“白名单”/“黑名单”**

“白名单”和“黑名单”术语已从Adobe Campaign文档中删除。 这些产品UI、选项名称和内部代码中可能仍然存在这些术语的某些出现，但在即将发布的活动版本中，这些术语将替换为“blocklist”和“allowlist”。

**活动用户档案监视**

控制面板现在允许您监视实例使用的活动用户档案数，并计数用于计费目的。 [阅读更多](performance-monitoring/using/active-profiles-monitoring.md)

>[!IMPORTANT]
>
>控制面板中的活动用户档案监视功能在测试版中可用，如有频繁更新和修改，恕不另行通知。
>
>该功能适用于在AWS上托管的从Campaign Standard10368构建和Campaign Classic8931构建开始的客户。 如果您使用的是以前的版本，则需要升级才能使用此功能。

## 2020年5月 {#may-2020}

**CNAME 子域的证书管理**

控制面板现在允许您续订已使用 CNAME 方法委派的子域的 SSL 证书。[阅读更多](subdomains-certificates/using/renewing-subdomain-certificate.md)

## 2020 年 4 月 {#april-2020}

**Google TXT 记录管理**

将 Google TXT 网站验证记录添加到所有子域，这些子域用于通过 Campaign 控制面板向 Gmail 地址发送电子邮件。[阅读更多](subdomains-certificates/using/managing-txt-records.md)

**数据库空间监控**

Campaign 控制面板配备了数据库监控功能，允许您查看按需数据库空间利用率以及随时间推移的利用率。[阅读更多](performance-monitoring/using/database-monitoring.md)

**电子邮件警报**

Campaign 控制面板具备实时电子邮件警报功能，您可以登录控制面板并注册，以在系统面临性能下降风险时接收警报，或者需要采取措施以确保未来的高性能时接收警报。[阅读更多](performance-monitoring/using/email-alerting.md)

## 2020 年 1 月 {#january-2020}

*2020 年 1 月 22 日*

我们为管理员用户添加了新功能，以便从控制面板委派子域和续订 SSL 证书。

有关详细信息，请参阅以下页面：
* [设置新子域](subdomains-certificates/using/setting-up-new-subdomain.md)
* [续订子域的 SSL 证书](subdomains-certificates/using/renewing-subdomain-certificate.md)

>[!IMPORTANT]
>
>这些功能将在测试版中提供，如有频繁更新和修改，恕不另行通知。

## 2019 年 9 月 {#september-2019}

*2019 年 9 月 16 日*

我们为管理员用户添加了新功能，以向允许列表添加IP地址，以便连接到Campaign Classic实例。
此外，管理员用户现在可以查看 Campaign Classic 实例的列表和具有版本升级资格。

有关详细信息，请参阅[专用文档](instances-settings/using/ip-whitelisting-instance-access.md)。

## 2019 年 8 月 {#august-2019}

我们添加了新功能，使管理员用户在域的 SSL 证书过期前接收通知。有关详细信息，请参阅[详细文档](subdomains-certificates/using/monitoring-ssl-certificates.md)。

此外，管理员用户现在可以删除为访问 SFTP 服务器而添加的 SSH 密钥。

## 2019 年 7 月 {#july-2019}

我们添加了新功能，使管理员用户能够更好地控制 Campaign Classic 实例设置。新的控制面板功能包括添加 Adobe Campaign 连接到的 URL 以进行数据/文件传输。

有关详细信息，请参阅[详细文档](instances-settings/using/url-permissions.md)。
