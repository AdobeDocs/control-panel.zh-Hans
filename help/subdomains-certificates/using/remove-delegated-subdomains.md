---
product: campaign
solution: Campaign
title: 移除子域委派
description: 了解如何移除对 Adobe 的子域委派。
feature: Control Panel, Subdomains and Certificates
role: Admin
level: Experienced
exl-id: 517818c9-8557-49fd-b49c-b98b60e48f1c
source-git-commit: a3485766791387bd9422b4f29daf86296efafb98
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# 移除对 Adobe 的子域委派 {#remove-delegated--subdomains}

>[!CONTEXTUALHELP]
>id="cp_subdomain_undelegate"
>title="移除子域委派"
>abstract="借助此屏幕，您可以移除对 Adobe 的子域委派。请记住，此过程在执行完成之前无法撤消，并且不可逆。<br><br>如果您尝试移除所选实例的主域委派，将会提示您选择替换它的域。"

通过“控制面板”，您可以移除已完全委派给 Adobe 的子域委派或使用 CNAME 委派的子域委派。

## 重要说明 {#important}

在继续之前，请仔细考虑移除过程触发后所产生的影响：

* 一旦触发该过程，在执行完成之前，子域委派移除操作将无法撤消并且不可逆。
* 当另一个子域正在进行类似的过程时，无法移除其他子域委派。
* 在子域上移除的委派只有在移除 3 天后才能重新委派。

## 移除子域委派 {#steps}

要移除对 Adobe 的子域委派，请执行以下步骤：

1. 单击要移除的域委派旁边的省略号按钮，然后选择&#x200B;**[!UICONTROL 移除委派]**。

   ![](assets/undelegate-subdomain.png)

1. 查看免责声明，确认移除对 Adobe 的域委派。

1. 查看有关与子域关联的实例的信息，包括相关的 IP 亲和度和品牌配置。

   如果您要移除所选实例的主域委派，则需要使用&#x200B;**[!UICONTROL 替换域]**&#x200B;列表选择用于替换它的域。

   单击&#x200B;**[!UICONTROL 下一步]**&#x200B;以继续移除。

   ![](assets/undelegate-subdomain-details.png)

1. 如果要移除 CNAME 类型委派，或者将主域替换为使用 CNAME 委派的域，则会显示一个额外的&#x200B;**[!UICONTROL 操作]**&#x200B;步骤，用于管理 DNS 记录。[在本节中了解详情](#dns)

1. 查看显示的摘要。要确认移除，请键入要移除委派的域 URL，然后单击&#x200B;**[!UICONTROL 提交]**。

   ![](assets/undelegate-submit.png)

开始移除委派后，待处理作业会一直显示在作业日志中，直到完成为止。

![](assets/undelegate-job.png)

## DNS 记录管理 {#dns}

要使用 CNAME 配置域委派，“控制面板”会要求您在 DNS 服务器上添加特定记录。[了解如何使用 CNAME 设置子域](setting-up-new-subdomain.md#use-cnames)

删除 CNAME 类型委派时，您需要从服务器中&#x200B;**移除这些 DNS 记录**&#x200B;以免出现任何问题。此外，如果您要移除主子域的委派，并将其替换为已使用 CNAME 委派的域，则可能需要在服务器中&#x200B;**添加 DNS 记录**，具体取决于为子域设置的 IP 亲和度。

下表列出了要执行的操作，具体取决于您要移除的委派类型以及用于设置替换域的委派类型。

| 已移除委派 | 替换域委派 | 所需操作 |
|  ---  |  ---  |  ---  |
| CNAME | 无替换域 | 删除 DNS 记录 |
| CNAME | CNAME | 删除 DNS 记录<br/>添加 DNS 记录&#x200B;*（可选项，具体取决于 IP 亲和度）* |
| CNAME | 完全 | 删除 DNS 记录 |
| 完全 | 无替换域 | 无需执行任何操作 |
| 完全 | CNAME | 添加 DNS 记录&#x200B;*（可选项，具体取决于 IP 亲和度）* |
| 完全 | 完全 | 无需执行任何操作 |

{style="table-layout:auto"}

如果需要执行其中一项操作来移除委派，则在确认移除委派前会显示一个额外的 **[!DNL Action]** 步骤。此屏幕列出了要移除或添加的 DNS 记录，具体取决于上下文。

![](assets/action-step.png)

### 删除 DNS 记录

1. 导航到 DNS 服务器，并在“控制面板”中移除列出的记录。
1. 返回控制面板并单击&#x200B;**[!UICONTROL 下一步]**&#x200B;以继续移除委派。

### 添加 DNS 记录

1. 导航到 DNS 服务器，并在“控制面板”中添加列出的记录。
1. 等待添加的 DNS 生效。
1. 返回控制面板并单击&#x200B;**[!UICONTROL 验证]**。
1. 添加的记录成功通过验证后，单击&#x200B;**[!UICONTROL 下一步]**&#x200B;以继续移除委派。

## 错误代码 {#FAQ}

此部分列出了在尝试移除子域委派时可能遇到的错误消息：

| 错误代码 | 消息 | 说明 |
|  ---  |  ---  |  ---  |
| 8002 | 无法处理请求的委派域移除操作，因为正在进行类似的重叠请求，请在 3 天后重试 | 所选实例的子域委派移除作业已在处理中。等待 3 天以开始新的删除作业。 |
| 8003 | 此实例不支持请求的委派域移除操作。 | 由于技术问题，所选子域不支持移除委派，请联系客户关怀团队。 |
| 8004 | 不允许请求的委派域移除操作，因为此实例中只有一个域。 | 只为所选实例委派了一个子域。不允许移除委派。 |
| 8005 | 此配置不支持请求的委派域移除操作。 | 由于技术问题，所选子域不支持移除委派，请联系客户关怀团队。 |
| 8006 | 由于未知原因，不允许请求的委派域移除操作。请联系客户关怀团队。 | 由于未知问题，所选实例不支持移除委派，请联系客户关怀团队。 |
