---
product: campaign
solution: Campaign
title: 删除子域的委派
description: 了解如何移除将子域委派给Adobe的过程。
feature: Control Panel
role: Architect
level: Experienced
source-git-commit: deb99ceb789f40c905de1a76cca8deca6b979765
workflow-type: tm+mt
source-wordcount: '498'
ht-degree: 12%

---

# 删除向Adobe委派子域 {#remove-delegated--subdomains}

>[!CONTEXTUALHELP]
>id="cp_subdomain_undelegate"
>title="移除子域委派"
>abstract="利用此屏幕，可删除要Adobe的子域委派。 请记住，此过程在执行完成之前无法撤消，并且不可逆。<br><br>如果您尝试删除所选实例的主域委派，将要求您选择替换它的域。"

控制面板允许您删除已委派给Adobe的子域的委派，包括CNAME设置。

## 重要说明 {#important}

在继续之前，请仔细考虑删除过程触发后所产生的影响：

* 一旦触发该流程，子域委派删除操作将无法撤消，并且在该流程执行完成之前不可撤消。
* 当另一个子域正在进行类似的过程时，无法删除其他子域委派。
* 在子域上移除的委派只有在移除3天后才能重新委派。

## 删除子域委派 {#steps}

要删除要Adobe的子域委派，请执行以下步骤：

1. 单击要删除的域委派旁边的省略号按钮，然后选择 **[!UICONTROL Remove delegated subdomain]**.

   ![](assets/undelegate-subdomain.png)

1. 查看免责声明，确认删除了向Adobe的域委派。

1. 查看有关与子域关联的实例的信息，包括相关的IP亲和度和品牌配置。

   如果您正在删除所选实例的主域的委派，则需要使用选择将替换它的域 **[!UICONTROL Replacement Domain]** 列表。

   单击 **[!UICONTROL Next]** 以继续删除。

   ![](assets/undelegate-subdomain-details.png)

1. 查看显示的摘要。 要确认删除，请键入要删除其委派的域的URL，然后单击 **[!UICONTROL Submit]**.

   ![](assets/undelegate-submit.png)

开始删除委派后，待处理作业会一直显示在作业日志中，直到作业完成为止。

![](assets/undelegate-job.png)

## 错误代码 {#FAQ}

本节列出了在尝试删除子域委派时可能遇到的错误消息：

| 错误代码 | 消息 | 说明 |
|  ---  |  ---  |  ---  |
| 8002 | 无法移除请求的委派域，因为有一个类似的重叠请求正在进行中，请在3天后重试 | 所选实例的子域委派删除作业已在处理中。 等待3天以开始新的删除作业。 |
| 8003 | 此实例不支持请求的委派域移除操作。 | 由于技术问题，所选子域不支持删除委派，请联系客户关怀团队。 |
| 8004 | 不允许请求的委派域移除操作，因为此实例中只有一个域。 | 只为选定的实例委派了一个子域。 不允许删除委派。 |
| 8005 | 此配置不支持请求的委派域移除操作。 | 由于技术问题，所选子域不支持删除委派，请联系客户关怀团队。 |
| 8006 | 由于未知原因，不允许请求的委派域移除操作。请联系客户关怀部门。 | 由于未知问题，选定实例不支持删除委派，请联系客户关怀团队。 |
