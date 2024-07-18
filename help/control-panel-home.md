---
title: 产品文档
description: 控制面板文档。
feature: Control Panel
role: Admin
level: Experienced
exl-id: 2b2cfaed-e42e-4c3a-a8d8-224b936890ab
source-git-commit: e8bffd8e7f571fd85c725adf837c2997f7615fcd
workflow-type: tm+mt
source-wordcount: '248'
ht-degree: 100%

---

# 帮助中心 {#control-panel-documentation}

>[!CONTEXTUALHELP]
>id="cp_overview"
>title="关于控制面板"
>abstract="通过控制面板主页，您可以访问可在 Campaign 实例上执行的所有操作。"
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/discover-control-panel/accessing-control-panel.html?lang=zh-Hans" text="访问控制面板"

Campaign 控制面板可用于管理每个 Campaign 实例的设置并跟踪使用情况，从而帮助 Campaign Standard 和 Campaign v7/v8 的产品管理员提高工作效率。

## 新增功能

**用户界面**

* 控制面板现在具有更多语言版本。[了解详情](discover/using/discovering-the-interface.md#supported-languages-languages)

**活动用户档案监测**

* 现在可以监测您有权访问的贵组织的活动用户档案数量，而且如果您正在使用多个实例，还可以监测所有实例中在贵组织内使用的用户档案总数。[了解详情](performance-monitoring/using/active-profiles-monitoring.md)

**DMARC 记录**

* 多个电子邮件地址现在可以接收汇总报告和故障报告电子邮件。[了解详情](subdomains-certificates/using/dmarc.md)
* 对于某个子域同时有 DMARC 和 BIMI 记录的情况，做出了如下变更：

   * 无法删除 DMARC 记录。如果要删除一个此类记录，则需要先删除 BIMI 记录。
   * DMARC 记录可以编辑，但不允许将策略降级为“无”，其百分比值必须为 100。

>[!CAUTION]
>
>* 控制面板仅限管理员用户使用。[了解详情](https://experienceleague.adobe.com/docs/control-panel/using/discover-control-panel/managing-permissions.html?lang=zh-Hans#discover-control-panel)
>
>* 对于 Campaign v7，部署限制适用。 [了解详情](faq.md#v7-restrictions)

## 其他资源 {#additional-resources}

<table>
    <tr>
        <td><b>Campaign Standard</b><br/>
        <ul>
            <li><a href="https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/control-panel-overview.html?lang=zh-Hans">控制面板教程视频</a></li>
            <li><a href="https://experienceleague.adobe.com/docs/campaign-standard/using/campaign-standard-home.html?lang=zh-Hans">Campaign Standard 产品文档</a></li>
        </ul>
        </td>
        <td><b>Campaign v7</b><br/>
        <ul>
            <li><a href="https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/control-panel-overview.html?lang=zh-Hans">控制面板教程视频</a></li>
            <li><a href="https://experienceleague.adobe.com/docs/campaign-classic/using/campaign-classic-home.html?lang=zh-Hans">Campaign v7 产品文档</a></li>
        </ul>
        </td>
        <td><b>Campaign v8</b><br/>
        <ul>
            <li><a href="https://experienceleague.adobe.com/docs/campaign-learn/control-panel/control-panel-overview.html?lang=zh-Hans">控制面板教程视频</a></li>
            <li><a href="https://experienceleague.adobe.com/docs/campaign/campaign-v8/campaign-home.html?lang=zh-Hans">Campaign v8 产品文档</a></li>
        </ul>
        </td>
    </tr>
</table>
