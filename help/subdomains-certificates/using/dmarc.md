---
product: campaign
solution: Campaign
title: 添加DMARC记录
description: 了解如何为子域添加DMARC记录。
feature: Control Panel
role: Architect
level: Experienced
source-git-commit: f87a13c8553173e4303c9b95cfea5de05ff49cee
workflow-type: tm+mt
source-wordcount: '693'
ht-degree: 0%

---


# 添加DMARC记录 {#dmarc}

## 关于DMARC记录 {#about}

基于域的邮件身份验证、报告和符合性(DMARC)是一种电子邮件身份验证协议标准，可帮助组织保护其电子邮件域免受网络钓鱼和欺骗攻击。 它允许您决定邮箱提供商应如何处理未通过SPF和DKIM检查的电子邮件，从而提供一种验证发件人域并防止未经授权而恶意使用域的方法。

<!--Detailed information on DMARC implementation is available in [Adobe Deliverability Best Practice Guide](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/technotes/implement-bimi.html)-->

## 限制和先决条件 {#limitations}

* SPF和DKIM记录是创建DMARC记录的先决条件。
* 只能使用完全子域委派为子域添加DMARC记录。 [了解有关子域配置方法的更多信息](subdomains-branding.md#subdomain-delegation-methods)

## 为子域添加DMARC记录 {#add}

要为子域添加DMARC记录，请执行以下步骤：

1. 从子域列表中，单击所需子域旁边的省略号按钮，然后选择 **[!UICONTROL Subdomain details]**.

1. 单击 **[!UICONTROL Add TXT record]** 按钮，然后选择 **[!UICONTROL DMARC]** 从 **[!UICONTROL Record Type]** 下拉列表。

   ![](assets/dmarc-add.png)

1. 选择 **[!UICONTROL Policy Type]** 当您的电子邮件之一失败时，收件人服务器应遵循的规则。 可用的策略类型包括：

   * **[!UICONTROL None]**，
   * **[!UICONTROL Quarantine]** （垃圾邮件文件夹放置），
   * **[!UICONTROL Reject]** （阻止电子邮件）。

   作为最佳实践，建议您逐步推出DMARC实施，方法是将DMARC策略从p=none提升到p=quarantine，再提升到p=reject，以便让DMARC了解DMARC的潜在影响。

   * **第1步：** 分析您收到并使用的反馈(p=none)，这告知接收者不对身份验证失败的邮件执行任何操作，但仍会向发件人发送电子邮件报告。 此外，如果合法消息未通过身份验证，请查看和修复SPF/DKIM的问题。

   * **第2步：** 确定SPF和DKIM是否一致并通过所有合法电子邮件的身份验证，然后将策略移至(p=quarantine)，这会告知接收电子邮件服务器隔离身份验证失败的电子邮件（这通常意味着将这些邮件放入垃圾邮件文件夹）。 如果策略设置为隔离，则建议您从一小部分电子邮件开始。

   * **步骤3：** 将策略调整为（p=拒绝）。 注意：请谨慎使用此策略，并确定它是否适合您的组织。 p=拒绝策略告知接收者完全拒绝（退回）验证失败的域的任何电子邮件。 启用此策略后，只有经域验证为100%经过身份验证的电子邮件才有机会放置收件箱。

   >[!NOTE]
   >
   > DMARC记录策略类型设置为“无”时，无法创建BIMI记录。

1. 填写应接收DMARC报告的电子邮件地址。 当您的其中一封电子邮件失败时，会自动将DMARC报告发送到您选择的电子邮件地址：

   * 汇总DMARC报表可提供高级信息，例如给定时间段内失败的电子邮件数量。
   * 取证DMARC故障报告提供了详细信息，例如故障电子邮件来自哪个IP地址。

1. 如果DMARC策略设置为“无”，请输入适用于100%电子邮件的百分比。

   如果策略设置为“拒绝”或“隔离”，建议您从一小部分电子邮件开始。 当来自您的域的更多电子邮件通过接收服务器的身份验证时，请使用较高的百分比缓慢更新您的记录。

   >[!NOTE]
   >
   >如果您的域使用BIMI，则DMARC策略的百分比值必须为100%。 BIMI不支持将此值设置为小于100%的DMARC策略。

   ![](assets/dmarc-add2.png)

1. DMARC报告每24小时发送一次。 您可以在中更改报表发送频率 **[!UICONTROL Reporting Interval]** 字段。 最小授权间隔为1小时，最大授权值为2190小时（即3个月）。

1. 在 **SPF** 和 **[!UICONTROL DKIM Identifier Alignment]** 字段，指定检查电子邮件的SPF和DKIM身份验证时收件人服务器的严格程度。

   * **[!UICONTROL Relaxed]** 模式：即使电子邮件是从子域发送的，服务器也接受身份验证，
   * **[!UICONTROL Strict]** 仅当发送方域与SPF和DKIM域完全匹配时，模式才接受身份验证。

   假设我们正在与 `http://www.luma.com` 域。 在“宽松”模式下，来自 `marketing.luma.com` 子域将由服务器进行授权，而它们将在“严格”模式下被拒绝。

1. 单击 **[!UICONTROL Add]** 以确认创建DMARC记录。

处理DMARC记录创建（大约5分钟）后，该记录会显示在子域的详细信息屏幕中。 [了解如何监测子域的TXT记录](gs-txt-records.md#monitor)