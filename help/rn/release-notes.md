---
title: 最新版本
description: 本页列出了所有新增功能和改进控制面板
exl-id: 13aceffb-ceaa-4cfe-8741-95d66c5c6caa
source-git-commit: daa52035ea5db89552b56afc4ab5690610b6e846
workflow-type: tm+mt
source-wordcount: '501'
ht-degree: 47%

---

# 最新版本 {#control-panel-releases}

本页列出了所有新增功能和改进控制面板。

## 2022 年 6 月 {#june-2022}

### 新增功能?

<table>
<thead>
<tr>
<th><strong>SFTP服务器上占用空间的前10个文件</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以识别SFTP服务器上占用空间最多的前10个文件。 <a href="../sftp/using/sftp-storage-management.md">了解详情</a></p>
<img src="../assets/do-not-localize/sftp.gif"/>
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
<p>“服务日历”现在允许您设置提醒，以便在实例中发生事件之前通过电子邮件通知您。 <a href="../service-events/service-events.md">了解详情</a></p>
<img src="../assets/do-not-localize/reminders.gif"/>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>子域的CSR生成增强功能</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>对CSR生成过程进行了一些增强。 <a href="../subdomains-certificates/using/renewing-subdomain-certificate.md">了解详情</a></p><ul><li>现在，在生成CSR时，您可以选择其中一个包含的子域作为通用名称。</li><li>现在，您可以在生成CSR之前复制CSR摘要。</li><li>生成CSR后，您可以从作业日志中再次下载它。 此功能不适用于在此版本之前生成的证书。</li></ul><p>
<img src="../assets/do-not-localize/CSR.gif"/>
</td>
</tr>
</tbody>
</table>

### 改进

**实例设置**

* 控制面板中GPG密钥的最大数量已增加到60个密钥。 [了解详情](../instances-settings/using/gpg-keys-management.md)

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
<p>控制面板现在可供具有混合托管模型的客户使用。这些客户可以通过在控制面板中提供他们在营销实例中配置的 MID/RT 实例 URL 来利用控制面板的功能。</p><p>有关更多信息，请参阅 <a href="../instances-settings/using/external-accounts.md">详细文档。</a></p>
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
<p>吞吐量和延迟监控功能已得到增强：<ul><li>您现在可以识别对实例吞吐量贡献最大的前 5 个投放的 ID。</li><li>Campaign Classic v7/v8 客户现在可以查看特定渠道的延迟。</p></li><p>有关更多信息，请参阅 <a href="../performance-monitoring/using/thoughputs-latencies.md">详细文档。</a></p>
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
<p>现可监控实例中发生的过去和即将推出的版本发布和服务评审，以及访问 Adobe 关键联系人列表，以便提出任何请求或问题。 </p><p>有关更多信息，请参阅 <a href="../service-events/service-events.md">详细文档。</a></p>
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
<p>现在，所有Campaign Standard和v8客户以及内部版本号为9032、9330、9346或9349且具有独立部署（无任何中间实例）的Campaign V7客户都可以使用吞吐量和延迟监控。</p><p>有关更多信息，请参阅 <a href="../performance-monitoring/using/thoughputs-latencies.md">详细文档。</a></p>
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
<p>您现在可以监测在实例上一段时间内的投放吞吐量和延迟趋势。</p><p>有关更多信息，请参阅<a href="../performance-monitoring/using/thoughputs-latencies.md">详细文档</a>。</p>
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
<p>现在，即使可交付性审核仍在进行中，也可以对新设置的子域执行SSL证书操作。</p><p>有关更多信息，请参阅<a href="../subdomains-certificates/using/renewing-subdomain-certificate.md">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>
