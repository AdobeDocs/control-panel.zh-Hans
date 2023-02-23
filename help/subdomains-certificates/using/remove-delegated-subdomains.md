---
product: campaign
solution: Campaign
title: 删除子域的委派
description: 了解如何删除子域委派以Adobe。
feature: Control Panel
role: Architect
level: Experienced
source-git-commit: 5a8c4c4d1c5c527135901cd41f2b0936af8737b4
workflow-type: tm+mt
source-wordcount: '493'
ht-degree: 2%

---

# 删除子域的委派以Adobe {#remove-delegated--subdomains}

>[!CONTEXTUALHELP]
>id="cp_subdomain_undelegate"
>title="删除子域委派"
>abstract="利用此屏幕，可移除子域的委派Adobe。 请记住，提交后，此过程将无法撤消或停止。<br><br>如果您尝试为所选实例删除主域的委派，将要求您选择将替换该实例的域。"

控制面板允许您删除已委派给Adobe的子域的委派，包括CNAME设置。

## 重要说明 {#important}

在继续操作之前，请仔细考虑在触发删除流程后所发生的影响：

* 子域委派删除无法撤消，在进程执行开始之前，子域委派删除将一旦启动，将不可撤消。
* 当另一个子域上的类似进程正在进行时，无法删除其他子域委派。
* 在子域上删除的委派在被删除3天后才能重新委派。

## 删除子域委派 {#steps}

要删除子域的委派Adobe，请执行以下步骤：

1. 单击要删除的域委派旁边的省略号按钮，然后选择 **[!UICONTROL Remove delegated subdomain]**.

   ![](assets/undelegate-subdomain.png)

1. 查看免责声明并确认删除了域委派以Adobe。

1. 查看有关子域关联到的实例的信息，包括相关的IP相关性和品牌配置。

   如果要删除所选实例的主域的委派，则需要选择将使用 **[!UICONTROL Replacement Domain]** 列表。

   单击 **[!UICONTROL Next]** 以继续删除。

   ![](assets/undelegate-subdomain-details.png)

1. 查看显示的摘要。 要确认删除，请键入要删除委派的域的URL并单击 **[!UICONTROL Submit]**.

   ![](assets/undelegate-submit.png)

启动委派删除后，待处理作业会显示在作业日志中，直到完成为止。

![](assets/undelegate-job.png)

## 错误代码 {#FAQ}

本节列出了在尝试删除子域的委派时可能遇到的错误消息：

| 错误代码 | 消息 | 说明 |
|  ---  |  ---  |  ---  |
| 8002 | 请求的委派域删除无法解决，因为存在类似的重叠请求，请在3天后尝试 | 所选实例的子域委派删除作业已在处理中。 等待3天以开始新的删除作业。 |
| 8003 | 此实例不支持请求的委派域移除。 | 由于技术问题，不支持对所选子域删除委派，请联系客户关怀团队。 |
| 8004 | 不允许删除请求的委派域，因为此实例中只有一个域。 | 只为所选实例委派了一个子域。 不允许删除委派。 |
| 8005 | 此配置不支持删除请求的委派域。 | 由于技术问题，不支持对所选子域删除委派，请联系客户关怀团队。 |
| 8006 | 由于未知原因，不允许删除请求的委派域。 请联系客户关怀团队。 | 由于未知问题，选定实例不支持删除委派，请联系客户关怀团队。 |
