---
title: 最新版本
description: 此页面列出了控制面板的所有新增功能和改进。
feature: Control Panel, Release Notes
role: Admin
level: Experienced
exl-id: 13aceffb-ceaa-4cfe-8741-95d66c5c6caa
source-git-commit: a3485766791387bd9422b4f29daf86296efafb98
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# 最新版本 {#control-panel-releases}

此页面列出了控制面板的所有新增功能和改进。

## 2023 年 10 月 {#october-2023}

**用户界面**

* 控制面板现在具有更多语言版本。[了解详情](../discover/using/discovering-the-interface.md#supported-languages-languages)

**活动用户档案监测**

* 现在可以监测您有权访问的贵组织的活动用户档案数量，而且如果您正在使用多个实例，还可以监测所有实例中在贵组织内使用的用户档案总数。[了解详情](../performance-monitoring/using/active-profiles-monitoring.md)

**DMARC 记录**

* 多个电子邮件地址现在可以接收汇总报告和故障报告电子邮件。[了解详情](../subdomains-certificates/using/dmarc.md)
* 对于某个子域同时有 DMARC 和 BIMI 记录的情况，做出了如下变更：

   * 无法删除 DMARC 记录。如果要删除一个此类记录，则需要先删除 BIMI 记录。
   * DMARC 记录可以编辑，但不允许将策略降级为“无”，其百分比值必须为 100。

