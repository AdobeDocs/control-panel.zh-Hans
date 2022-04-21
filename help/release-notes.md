---
product: campaign
solution: Campaign
title: 控制面板版本
description: 本页列出了所有新增功能和改进控制面板
exl-id: 13aceffb-ceaa-4cfe-8741-95d66c5c6caa
source-git-commit: da68420340ea8605f6e1347e86797c9e6a790ea6
workflow-type: tm+mt
source-wordcount: '1070'
ht-degree: 60%

---

# 控制面板版本 {#control-panel-releases}

本页列出了所有新增功能和改进控制面板。

>[!NOTE]
>
>控制面板仅供管理员用户访问。 了解有关 [此部分](https://experienceleague.adobe.com/docs/control-panel/using/discover-control-panel/managing-permissions.html?lang=zh-Hans#discover-control-panel).
>
>对于Campaign v7，您的实例必须托管在Amazon Web Services(AWS)上并升级到最新版本 [营销活动稳定内部版本](https://experienceleague.adobe.com/docs/campaign-classic/using/release-notes/rn-overview.html?lang=zh-Hans#rn-statuses) （或构建9032或更高版本）。 在[本节](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/starting-with-adobe-campaign/launching-adobe-campaign.html?lang=zh-Hans#getting-your-campaign-version)中了解如何确认您的版本。要检查您的实例是否托管在 AWS 上，请按照[此页面](faq.md#hosted-aws)中详述的步骤操作。

## 2022 年 4 月 {#april-2022}

<table>
<thead>
<tr>
<th><strong>监控实例上的关键联系人和事件</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以监控实例上发生的过去和即将发布的版本和服务审核，以及在Adobe访问任何请求或问题的关键联系人列表。</p><p>有关更多信息，请参阅 <a href="service-events/service-events.md">详细文档。</a></p>
</td>
</tr>
</tbody>
</table>

## 2022 年 3 月 {#march-2022}

<table>
<thead>
<tr>
<th><strong>吞吐量和延迟监控可用性</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>现在，所有Campaign Standard和v8客户以及内部版本号为9032、9330、9346或9349且具有独立部署（无任何中间实例）的Campaign V7客户都可以使用吞吐量和延迟监控。</p><p>有关更多信息，请参阅 <a href="performance-monitoring/using/thoughputs-latencies.md">详细文档。</a></p>
</td>
</tr>
</tbody>
</table>

## 2022 年 2 月 {#february-2022}

<table>
<thead>
<tr>
<th><strong>工作流参数监测</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以监测可能需要特别关注的工作流参数，以避免实例上出现任何问题。 </p><p>有关更多信息，请参阅<a href="performance-monitoring/using/workflow-monitoring.md">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>

## 2022 年 1 月 {#january-2022}

<table>
<thead>
<tr>
<th><strong>活动查询监测</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>控制面板现在允许您监测在实例上运行时间最长的查询。</p><p>有关更多信息，请参阅<a href="performance-monitoring/using/database-active-queries.md">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>吞吐量和延迟监测</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以监测在实例上一段时间内的投放吞吐量和延迟趋势。</p><p>有关更多信息，请参阅<a href="performance-monitoring/using/thoughputs-latencies.md">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>对新子域执行SSL证书操作</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>现在，即使可交付性审核仍在进行中，也可以对新设置的子域执行SSL证书操作。</p><p>有关更多信息，请参阅<a href="subdomains-certificates/using/renewing-subdomain-certificate.md">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>

## 2021 年 10 月 {#october-2021}

<table>
<thead>
<tr>
<th><strong>IP范围和公钥有效期</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>现在，可以设置IP范围和公共密钥可用性的持续时间。 </p><p>有关更多信息，请参阅 <a href="sftp/using/ip-range-allow-listing.md#adding-ip-addresses-allow-list">IP范围允许列表</a> 和 <a href="sftp/using/key-management.md#installing-ssh-key">密钥管理</a> 中。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>IP范围和公钥版本</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以编辑 <a href="sftp/using/ip-range-allow-listing.md#editing-ip-ranges">IP范围</a> 和 <a href="sftp/using/key-management.md#editing-public-keys">公共密钥</a> 创建的。 请注意，此功能不适用于在当前控制面板版本之前创建的项目。
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>SFTP IP范围和公钥到期警报</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>电子邮件警报功能现在包含有关SFTP IP允许列表过期和SFTP公钥过期的警报。</p><p>有关更多信息，请参阅<a href="performance-monitoring/using/email-alerting.md">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Campaign v8 提供全面支持</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>的 <strong>子域</strong> 和 <strong>证书</strong> Adobe Campaign v8上的控制面板现在支持管理功能。</a>.</p>
</td>
</tr>
</tbody>
</table>

## 2021 年 8 月 {#august-2021}

<table>
<thead>
<tr>
<th><strong>支持Campaign v8</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>控制面板现在可用于Adobe Campaign v8，但 <strong>子域</strong> 和 <strong>证书</strong> 管理功能，但尚不受支持。</p><p>有关更多信息，请参阅 <a href="https://experienceleague.adobe.com/docs/campaign/campaign-v8/deploy/self-service.html" target="blank">Campaign v8文档</a>.</p>
</td>
</tr>
</tbody>
</table>

## 2020 年 10 月 {#october-2020}

<table>
<thead>
<tr>
<th><strong>使用 CNAME 的子域配置</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>控制面板现在可让您配置子域以直接从界面使用 CNAME 处理 Adobe。</p><p>有关更多信息，请参阅<a href="subdomains-certificates/using/setting-up-new-subdomain.md">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>数据库监视增强功能</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>数据库监控已通过其他量度得到增强，这些量度允许您获取有关占用数据库空间的资源的详细信息。</p><p>有关更多信息，请参阅<a href="performance-monitoring/using/database-monitoring.md">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>

## 2020 年 6 月 {#june-2020}

<table>
<thead>
<tr>
<th><strong>子域可交付性审核</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>委派新子域后，控制面板现在允许您跟踪可交付性团队执行的审核。</p><p>有关更多信息，请参阅<a href="subdomains-certificates/using/setting-up-new-subdomain.md">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>GPG 密钥管理</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>现在，控制面板允许您生成一对 GPG 密钥，以便您可以从外部轻松解密进入 Campaign 的数据。此外，我们还添加了一项功能，以便您可以安装公共 GPG 密钥来加密离开 Campaign 的数据。</p><p>有关更多信息，请参阅<a href="instances-settings/using/gpg-keys-management.md">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>活动用户档案监测</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>控制面板现在允许您监控实例使用的活动用户档案数，并计数用于计费目的。</p><p>有关更多信息，请参阅<a href="performance-monitoring/using/active-profiles-monitoring.md">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>

>[!IMPORTANT]
>
>测试版中提供控制面板的活动用户档案监控，如有频繁更新和修改，恕不另行通知。

## 2020 年 5 月 {#may-2020}

<table>
<thead>
<tr>
<th><strong>CNAME 子域的证书管理</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>控制面板现在可让您续订已使用 CNAME 方式配置的子域的 SSL 证书。</p><p>有关更多信息，请参阅<a href="subdomains-certificates/using/renewing-subdomain-certificate.md">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>

## 2020 年 4 月 {#april-2020}

<table>
<thead>
<tr>
<th><strong>Google TXT 记录管理</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>将 Google TXT 网站验证记录添加到所有子域，这些子域用于通过 Campaign 控制面板向 Gmail 地址发送电子邮件。</p><p>有关更多信息，请参阅<a href="subdomains-certificates/using/managing-txt-records.md">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>数据库空间监控</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Campaign 控制面板配备了数据库监控功能，允许您查看按需数据库空间利用率以及随时间推移的利用率。</p><p>有关更多信息，请参阅<a href="performance-monitoring/using/database-monitoring.md">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>电子邮件警报</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Campaign 控制面板具备实时电子邮件警报功能，您可以登录控制面板并注册，以在系统面临性能下降风险时接收警报，或者需要采取措施以确保未来的高性能时接收警报。</p><p>有关更多信息，请参阅<a href="performance-monitoring/using/email-alerting.md">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>

## 2020 年 1 月 {#january-2020}

我们为管理员用户添加了新功能，以便从控制面板配置子域和续订 SSL 证书。

有关详细信息，请参阅以下页面：
* [设置新子域](subdomains-certificates/using/setting-up-new-subdomain.md)
* [续订子域的 SSL 证书](subdomains-certificates/using/renewing-subdomain-certificate.md)

>[!IMPORTANT]
>
>这些功能将在测试版中提供，如有频繁更新和修改，恕不另行通知。

## 2019 年 9 月 {#september-2019}

我们为管理员用户添加了新功能，以向允许列表添加IP地址，以便连接到Campaign v7/v8实例。
此外，管理员用户现在可以查看Campaign v7/v8实例的列表以及版本升级的资格。

有关详细信息，请参阅[专用文档](instances-settings/using/ip-allow-listing-instance-access.md)。

## 2019 年 8 月 {#august-2019}

我们添加了新功能，使管理员用户在域的 SSL 证书过期前接收通知。有关详细信息，请参阅[详细文档](subdomains-certificates/using/monitoring-ssl-certificates.md)。

此外，管理员用户现在可以删除为访问 SFTP 服务器而添加的 SSH 密钥。

## 2019 年 7 月 {#july-2019}

我们添加了新功能，使管理员用户能够更好地控制Campaign v7/v8实例设置。 新的控制面板功能包括添加 Adobe Campaign 连接到的 URL 以进行数据/文件传输。

有关详细信息，请参阅[详细文档](instances-settings/using/url-permissions.md)。
