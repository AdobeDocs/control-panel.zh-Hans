---
title: 控制面板版本
translation-type: tm+mt
source-git-commit: ef0a3ccdec2aec6f220a93ab474242df2d3a621b
workflow-type: tm+mt
source-wordcount: '372'
ht-degree: 0%

---


# 控制面板版本 {#control-panel-releases}

您将在此处找到有关最新Control Panel版本的信息。

>[!NOTE]
>
>请注意，控制面板仅适用于在AWS上托管的客户，但混合环境尚未受支持除外。 访问控制面板无需升级。 请确保您是管理员用户，可以访问它。

## 2020年5月 {#may-2020}

**CNAME子域的证书管理**

控制面板现在允许您续订已使用CNAME方法委派的子域的SSL证书。 [阅读更多](subdomains-certificates/using/renewing-subdomain-certificate.md)

## 2020年4月 {#april-2020}

**Google TXT记录管理**

将Google TXT站点验证记录添加到所有子域，这些子域用于通过活动控制面板向Gmail地址发送电子邮件。 [阅读更多](subdomains-certificates/using/managing-txt-records.md)

**数据库空间监视**

活动控制面板配备了数据库监视功能，允许您按需或随时间视图数据库空间利用率。 [阅读更多](performance-monitoring/using/database-monitoring.md)

**电子邮件警报**

活动控制面板具备实时电子邮件警报功能，允许您登录控制面板并在系统面临性能恶化风险或需要采取措施确保未来的高性能时注册接收警报。 [阅读更多](performance-monitoring/using/email-alerting.md)

## 2020年1月 {#january-2020}

*2020年1月22日*

我们为管理员用户添加了新功能，以便从控制面板委派子域和续订SSL证书。

有关详细信息，请参阅以下页面：
* [设置新子域](subdomains-certificates/using/setting-up-new-subdomain.md)
* [续订子域的SSL证书](subdomains-certificates/using/renewing-subdomain-certificate.md)

>[!IMPORTANT]
>
>这些功能将在测试版中提供，并且如有频繁更新和修改，恕不另行通知。

## 2019年9月 {#september-2019}

*2019年9月16日*

我们为管理员用户添加了新功能，将IP地址添加到白名单中以连接到Campaign Classic实例。
此外，管理员用户现在可以视图Campaign Classic实例的列表和构建升级资格。

有关详细信息，请参阅专 [用文档](instances-settings/using/ip-whitelisting-instance-access.md)。

## 2019年8月 {#august-2019}

我们为管理员用户添加了新功能，允许他们在域的SSL证书过期前接收通知。 有关详细信息，请参阅详 [细文档](subdomains-certificates/using/monitoring-ssl-certificates.md)。

此外，管理员用户现在可以删除已添加用于访问SFTP服务器的SSH密钥。

## 2019年7月 {#july-2019}

我们添加了新功能，使管理员用户能够更好地控制Campaign Classic实例设置。 新的控制面板功能包括添加Adobe Campaign连接到的URL以进行数据／文件传输。

有关详细信息，请参阅详 [细文档](instances-settings/using/url-permissions.md)。
