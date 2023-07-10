---
title: 2023 年版发行说明
description: 此页面列出了控制面板的所有 2023 年版本。
exl-id: 9a83e32a-4c11-4784-a6fe-341ce9ebc7a7
source-git-commit: 40654418f0c5b298cc4fbd66a5d835355876a12c
workflow-type: ht
source-wordcount: '242'
ht-degree: 100%

---

# 2023 年版发行说明 {#rn-2023}

## 2023 年 5 月改进 {#june-2023}

**对 Adobe 的子域 SSL 证书委派**

您现在可以使用 Adobe 管理子域的 SSL 证书。如果您使用 CNAME 设置您的子域，则将自动生成并提供证书记录，以便在您的域托管解决方案中生成证书。

请注意，仅在设置新子域时有此功能可用。无法为现有委派的子域委派证书。[了解详情](../subdomains-certificates/using/setting-up-new-subdomain.md)

>[!NOTE]
>
>Adobe 管理的 SSL 是一项免费功能，可供用户免费使用。

## 2023 年 3 月 {#march-2023}

**移除 CNAME 的子域委派**

现在，您可以移除已使用 CNAME 配置的子域委派。[了解详情](../subdomains-certificates/using/remove-delegated-subdomains.md)

## 2023 年 2 月 {#february-2023}

**移除委派给 Adobe 的子域委派**

您现在可以移除已完全委派给 Adobe 的子域委派。[了解详情](../subdomains-certificates/using/remove-delegated-subdomains.md)

>[!NOTE]
>
>目前，委派移除不适用于使用 CNAME 设置的子域。

**服务日历**

现在，服务日历提供日历视图，用于跟踪实例上发生的重要事件。此外，在向订阅“控制面板”警报的用户发送通知时添加了信息。[了解详情](../service-events/service-events.md)

![](assets/do-not-localize/gif-calendar.gif)

## 2023 年 1 月 {#january-2023}

**新的混合托管模型功能**

现在，具有混合托管模型的客户可以向允许列表添加 IP 地址以访问 MID 实例。[了解详情](../instances-settings/using/ip-allow-listing-instance-access.md)

**证书签名请求 (CSR) 增强功能**

现在，在生成证书签名请求时，“城市/地区”字段是可选项。