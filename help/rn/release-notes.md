---
title: 最新版本
description: 此页面列出了控制面板的所有新增功能和改进。
feature: Control Panel, Release Notes
role: Admin
level: Experienced
exl-id: 13aceffb-ceaa-4cfe-8741-95d66c5c6caa
TQID: 'https://experienceleague.adobe.com/Q1kU0q1e-a-H0LvAyK-5yYhfrUpGco1hVHWUsz-syhY'
product_v2:
  - id: dfc56824-e8b9-499e-85d4-21aedb507314
    internal-label: Campaign
feature_v2:
  - id: ae9127b0-c11d-467b-903d-a84cef43f6ed
    internal-label: Control Panel
  - id: c5474392-5419-4296-9e41-f6f4ce4f6e9b
    internal-label: Administration
subfeature_v2:
  - id: e5e477db-ebc7-4368-ab0f-4d8fc2aed405
    internal-label: Release notes
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: d378ca77-2da1-4f39-ad92-1917fe974a38
    internal-label: Experienced
source-git-commit: b2723b0683a305a992b710a37a3e47927e1fb65e
workflow-type: tm+mt
source-wordcount: '150'
ht-degree: 100%
---
# 最新版本 {#control-panel-releases}

此页面列出了控制面板的所有新增功能和改进。

## 2023 年 10 月 {#october-2023}

**用户界面**

* 控制面板现在具有更多语言版本。 [了解详情](../discover/using/discovering-the-interface.md#supported-languages-languages)

**活动轮廓监测**

* 现在可以监测您有权访问的贵组织的活动轮廓数量，而且如果您正在使用多个实例，还可以监测所有实例中在贵组织内使用的轮廓总数。 [了解详情](../performance-monitoring/using/active-profiles-monitoring.md)

**DMARC 记录**

* 多个电子邮件地址现在可以接收汇总报告和故障报告电子邮件。 [了解详情](../subdomains-certificates/using/dmarc.md)
* 对于某个子域同时有 DMARC 和 BIMI 记录的情况，做出了如下变更：

  * 无法删除 DMARC 记录。 如果要删除一个此类记录，则需要先删除 BIMI 记录。
  * DMARC 记录可以编辑，但不允许将策略降级为“无”，其百分比值必须为 100。

