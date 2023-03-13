---
product: campaign
solution: Campaign
title: 移除子域委派
description: 了解如何移除对 Adobe 的子域委派。
feature: Control Panel
role: Architect
level: Experienced
source-git-commit: 349eb8778a19263b83b70b8c920c401aff7fa24a
workflow-type: tm+mt
source-wordcount: '509'
ht-degree: 100%

---

# 移除对 Adobe 的子域委派 {#remove-delegated--subdomains}

>[!CONTEXTUALHELP]
>id="cp_subdomain_undelegate"
>title="移除子域委派"
>abstract="借助此屏幕，您可以移除对 Adobe 的子域委派。请记住，此过程在执行完成之前无法撤消，并且不可逆。<br><br>如果您尝试移除所选实例的主域委派，将会提示您选择替换它的域。"

通过“控制面板”，您可以移除已委派给 Adobe 的子域委派。

>[!NOTE]
>
>目前，委派移除不适用于使用 CNAME 设置的子域。

## 重要说明 {#important}

在继续之前，请仔细考虑移除过程触发后所产生的影响：

* 一旦触发该过程，在执行完成之前，子域委派移除操作将无法撤消并且不可逆。
* 当另一个子域正在进行类似的过程时，无法移除其他子域委派。
* 在子域上移除的委派只有在移除 3 天后才能重新委派。

## 移除子域委派 {#steps}

要移除对 Adobe 的子域委派，请执行以下步骤：

1. 单击要移除的域委派旁边的省略号按钮，然后选择 **[!UICONTROL Remove delegated subdomain]**。

   ![](assets/undelegate-subdomain.png)

1. 查看免责声明，确认移除对 Adobe 的域委派。

1. 查看有关与子域关联的实例的信息，包括相关的 IP 亲和度和品牌配置。

   如果您正在移除所选实例的主域委派，则需要使用 **[!UICONTROL Replacement Domain]** 列表选择替换它的域。

   单击 **[!UICONTROL Next]** 以继续移除。

   ![](assets/undelegate-subdomain-details.png)

1. 查看显示的摘要。要确认删除，请键入要移除委派的域 URL，然后单击 **[!UICONTROL Submit]**。

   ![](assets/undelegate-submit.png)

开始移除委派后，待处理作业会一直显示在作业日志中，直到完成为止。

![](assets/undelegate-job.png)

## 错误代码 {#FAQ}

此部分列出了在尝试移除子域委派时可能遇到的错误消息：

| 错误代码 | 消息 | 说明 |
|  ---  |  ---  |  ---  |
| 8002 | 无法处理请求的委派域移除操作，因为正在进行类似的重叠请求，请在 3 天后重试 | 所选实例的子域委派移除作业已在处理中。等待 3 天以开始新的删除作业。 |
| 8003 | 此实例不支持请求的委派域移除操作。 | 由于技术问题，所选子域不支持移除委派，请联系客户关怀团队。 |
| 8004 | 不允许请求的委派域移除操作，因为此实例中只有一个域。 | 只为所选实例委派了一个子域。不允许移除委派。 |
| 8005 | 此配置不支持请求的委派域移除操作。 | 由于技术问题，所选子域不支持移除委派，请联系客户关怀团队。 |
| 8006 | 由于未知原因，不允许请求的委派域移除操作。请联系客户关怀团队。 | 由于未知问题，所选实例不支持移除委派，请联系客户关怀团队。 |
