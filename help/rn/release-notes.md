---
title: 最新版本
description: 此页面列出了控制面板的所有新增功能和改进。
feature: Control Panel, Release Notes
role: Admin
level: Experienced
exl-id: 13aceffb-ceaa-4cfe-8741-95d66c5c6caa
source-git-commit: a3485766791387bd9422b4f29daf86296efafb98
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 26%

---

# 最新版本 {#control-panel-releases}

此页面列出了控制面板的所有新增功能和改进。

## 2023 年 10 月 {#october-2023}

**用户界面**

* 控制面板现在提供其他语言版本。 [了解详情](../discover/using/discovering-the-interface.md#supported-languages-languages)

**活动用户档案监控**

* 如果您使用多个实例，您现在可以监视您有权为组织使用的活动用户档案的数量，以及组织内所有实例中使用的用户档案总数。 [了解详情](../performance-monitoring/using/active-profiles-monitoring.md)

**DMARC记录**

* 多个电子邮件地址现在可以接收汇总报告和失败报告电子邮件。 [了解详情](../subdomains-certificates/using/dmarc.md)
* 如果子域同时存在DMARC和BIMI记录，则进行了更改：

   * 无法删除DMARC记录。 如果要删除一个，则需要先删除BIMI记录。
   * DMARC记录可以编辑，但策略降级为“无”是不允许的，其百分比值必须为100。

