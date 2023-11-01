---
title: 2022 年版发行说明
description: 此页面列出了控制面板的所有 2022 年版本。
feature: Control Panel, Release Notes
role: Admin
level: Experienced
exl-id: 9fb18bb6-c4e4-48aa-849c-d9129add5266
source-git-commit: a3485766791387bd9422b4f29daf86296efafb98
workflow-type: tm+mt
source-wordcount: '580'
ht-degree: 100%

---

# 2022 年版发行说明 {#rn-2022}

## 2022 年 10 月 {#october-2022}

现在，在您的某个 SSL 证书将在 30 天或更短时间内过期时，电子邮件警报会通知您。[了解详情](../performance-monitoring/using/email-alerting.md)

## 2022 年 9 月 {#september-2022}

现在，使用混合托管模型的客户可以设置新的子域。[了解详情](../subdomains-certificates/using/setting-up-new-subdomain.md)

## 2022 年 8 月 {#august-2022}

* 现在，使用混合托管模型的客户可以验证其子域。[了解详情](../subdomains-certificates/using/monitoring-subdomains.md)
* “Organization Unit (OU)”字段现在在证书生成请求 (CSR) 中为可选项。[了解详情](../subdomains-certificates/using/renewing-subdomain-certificate.md)

## 2022 年 7 月 {#july-2022}

<table>
<thead>
<tr>
<th><strong>用于混合托管模型的子域证书安装</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><p>现在，具有混合托管模型的客户可以从控制面板续订其子域的 SSL 证书。</p><p>有关详细信息，请参阅<a href="../subdomains-certificates/using/renewing-subdomain-certificate.md">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>

## 2022 年 6 月 {#june-2022}

### 新增功能？

<table>
<thead>
<tr>
<th><strong>SFTP 服务器上占用空间最多的前 10 个文件</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以识别 SFTP 服务器上占用空间最多的前 10 个文件。<a href="../sftp/using/sftp-storage-management.md">了解详情</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>服务日历提醒</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>现在，可使用“服务日历”设置提醒，以便在实例中发生事件之前通过电子邮件接收通知。<a href="../service-events/service-events.md">了解详情</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>子域的 CSR 生成过程增强</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>对 CSR 生成过程进行了一些增强。<a href="../subdomains-certificates/using/renewing-subdomain-certificate.md">了解详情</a></p><ul><li>现在，在生成 CSR 时，您可以选择其中一个包含的子域作为通用名称。</li><li>现在，您可以在生成 CSR 之前复制 CSR 摘要。</li><li>生成 CSR 后，您可以从作业日志中再次下载它。此功能不适用于在此版本之前生成的证书。</li></ul><p>

</td>
</tr>
</tbody>
</table>

### 改进

**实例设置**

* 控制面板中 GPG 密钥的最大数量已增加到 60 个。[了解详情](../instances-settings/using/gpg-keys-management.md)

## 2022 年 5 月 {#may-2022}

<table>
<thead>
<tr>
<th><strong>控制面板对混合托管模型的适用性</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>控制面板现在可供具有混合托管模型的客户使用。这些客户可以通过在控制面板中提供他们在营销实例中配置的 MID/RT 实例 URL 来利用控制面板的功能。</p><p>有关详细信息，请参阅<a href="../instances-settings/using/external-accounts.md">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>吞吐量和延迟监测更新</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>增强了吞吐量和延迟监测功能：<ul><li>您现在可以识别对实例吞吐量贡献最大的前 5 个投放的 ID。</li><li>Campaign Classic v7/v8 客户现在可以查看特定渠道的延迟。</p></li><p>有关详细信息，请参阅<a href="../performance-monitoring/using/throughputs-latencies.md">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>


## 2022 年 4 月 {#april-2022}

<table>
<thead>
<tr>
<th><strong>监测关键联系人和实例中的事件</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>现可监控实例中发生的过去和即将推出的版本发布和服务评审，以及访问 Adobe 关键联系人列表，以便提出任何请求或问题。</p><p>有关详细信息，请参阅<a href="../service-events/service-events.md">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>

## 2022 年 3 月 {#march-2022}

<table>
<thead>
<tr>
<th><strong>吞吐量和延迟可用性监测</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>吞吐量和延迟检测适用于所有 Campaign Standard 和 Campaign v8 客户，以及具有独立部署（不含任何中间实例）、内部版本号为 9032、9330、9346 或 9349 的 Campaign V7 客户。</p><p>有关详细信息，请参阅<a href="../performance-monitoring/using/throughputs-latencies.md">详细文档</a>。</p>
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
<p>您现在可以监测可能需要特别关注的工作流参数，以避免实例上出现任何问题。 </p><p>有关更多信息，请参阅<a href="../performance-monitoring/using/workflow-monitoring.md">详细文档</a>。</p>
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
<p>控制面板现在允许您监测在实例上运行时间最长的查询。</p><p>有关更多信息，请参阅<a href="../performance-monitoring/using/database-active-queries.md">详细文档</a>。</p>
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
<p>您现在可以监测在实例上一段时间内的投放吞吐量和延迟趋势。</p><p>有关更多信息，请参阅<a href="../performance-monitoring/using/throughputs-latencies.md">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>针对新子域的 SSL 证书操作</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>现在，即使可投放性审核仍在进行中，仍可对新设置的子域执行 SSL 证书操作。</p><p>有关更多信息，请参阅<a href="../subdomains-certificates/using/renewing-subdomain-certificate.md">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>
