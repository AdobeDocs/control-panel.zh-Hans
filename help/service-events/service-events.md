---
product: campaign
solution: Campaign
title: 识别关键联系人和事件
description: 了解如何识别实例上发生的事件和在 Adobe 的关键联系人。
feature: Control Panel, Monitoring
role: Admin
level: Intermediate
exl-id: d230aae6-4f0e-4201-bb3c-0e3f83a7c1b8
source-git-commit: a3485766791387bd9422b4f29daf86296efafb98
workflow-type: ht
source-wordcount: '781'
ht-degree: 100%

---

# 识别关键联系人和事件 {#keycontacts-events}

>[!CONTEXTUALHELP]
>id="cp_servicecalendar_serviceevents"
>title="服务日历"
>abstract="“关键联系人”部分列出了可联系的 Adobe 人员，以便您针对实例提出任何请求或问题。 在“Service Event Calendar”部分中，您可以确定过去/即将发布的版本以及有关选定实例的警报，并为特定事件设置提醒。"

>[!IMPORTANT]
>
>服务日历将在 Beta 版中提供，如有频繁更新和修改，恕不另行通知。

要有效监控 Campaign 实例，请务必跟踪可能会影响实例的重要事件。通过“控制面板”，您可以确定新版本、升级、补丁程序、修补程序等事件，还可获得有关任何请求或问题的关键 Adobe 联系人列表。

可在“控制面板”主页的&#x200B;**[!UICONTROL 服务日程表]**&#x200B;信息卡中获得此信息。

## 关键联系人 {#key-contacts}

**[!UICONTROL 关键联系人]**&#x200B;部分列出了可联系的 Adobe 人员列表，以便您针对实例提出任何请求或问题。

>[!NOTE]
>
>此部分仅显示“托管服务帐户”的信息。

![](assets/service-events-contacts.png)

主要联系人包括以下角色：

* **[!UICONTROL TAM]**：技术客户经理；
* **[!UICONTROL CSM]**：客户成功经理；
* **[!UICONTROL 可投放性]**：可投放性操作联系人；
* **[!UICONTROL 过渡经理]**：Managed Services 过渡经理（仅限 Managed Services 客户）；
* **[!UICONTROL 客户引导专家]**：分配给客户的专家，可帮助您熟悉 Campaign Classic（仅限 Managed Services 客户）。

## 跟踪重要事件 {#events}

**[!UICONTROL 服务事件日程表]**&#x200B;部分显示所有过去和即将发布的版本，以及用户在“控制面板”电子邮件警报中订阅的警报。此外，通过“控制面板”，用户可以为选定实例设置提醒并标记相关事件，以便更好地进行组织并提高效率。

事件显示在日历或列表中。您可以使用该部分中右上角的&#x200B;**[!UICONTROL 日程表]**&#x200B;和&#x200B;**[!UICONTROL 列表]**&#x200B;按钮在两个视图之间进行切换。

![](assets/service-events-calendar.png)

<table><tr style="border: 0;">
<td><img src="assets/do-not-localize/nav-buttons.png">
</td><td>在日历视图中，右上角是导航按钮，可帮助您浏览事件。使用<b>双箭头</b>导航到在选定月份之后/之前存在的第一个事件，使用<b>单箭头</b>从一个月导航到另一个月。单击<b>圆圈按钮</b>回到今天的视图。</td>
</tr></table>

显示的事件有三种类型：

* **提醒**&#x200B;由用户设置，以便在事件发生之前接收通知。这些在日历视图中以绿色显示。[了解如何设置提醒](#reminders)
* **警报**&#x200B;由“控制面板”通过电子邮件发送，以通知用户有关其实例的问题，如存储过载或 SSL 证书过期。这些在日历视图中以橙色显示。事件描述会说明是否向登录用户发送了警报，具体取决于他们的电子邮件警报订阅设置。[了解有关“控制面板”电子邮件警报功能的更多信息](../performance-monitoring/using/email-alerting.md)

* **版本**&#x200B;会指明实例过去和未来即将进行的部署，在日历视图中分别以灰色和蓝色显示。事件详细信息会说明与每个部署关联的版本类型：

   * **[!UICONTROL 正式发布版]**：最新发布的稳定版本。
   * **[!UICONTROL 有限发布版]**：仅限按需部署。
   * **[!UICONTROL 候选版本]**：已通过工程验证。正在等待生产校对。
   * **[!UICONTROL 预发行版]**：提前提供以满足特定客户需求。
   * **[!UICONTROL 不再可用]**：该版本不存在重大问题，但有修复了更多错误的新版本可供使用。需要进行升级。
   * **[!UICONTROL 已弃用]**：版本嵌入已知回退。不再支持该版本。 必须进行升级。

可为一个或多个即将发生的事件分配一个标记以进行跟踪。 要实现这一点，请单击事件名称旁边的省略号按钮。

![](assets/service-events-flag.png)

## 设置提醒 {#reminders}

使用“服务日历”，您可以设置提醒，以便在事件发生之前通过电子邮件接收通知。

>[!NOTE]
>
>要接收有关即将发生的事件的通知，请确保您已在控制面板中订阅电子邮件警报。[了解详情](../performance-monitoring/using/email-alerting.md)

要针对某一事件设置警报，请执行以下步骤：

1. 将鼠标悬停在要为其设置提醒的事件上，或单击列表视图中的椭圆按钮并选择&#x200B;**[!UICONTROL 设置提醒]**。

1. 为提醒设置一个标题，然后选择要在事件发生之前接收通知的日期。

   ![](assets/service-events-set-reminder.png)

   >[!NOTE]
   >
   >如果您未订阅控制面板警报，则会显示一条消息，您可以进行注册以接收电子邮件通知。

1. 现已为选定事件设置提醒。您可以随时将鼠标悬停在该事件上以显示其标题。

   ![](assets/service-events-reminder.png)

   >[!NOTE]
   >
   >您最多可以为同一事件设置 2 个提醒。

1. 在提醒中指定的日期，会发送一封电子邮件，通知您即将发生的事件，并将该提醒从“服务日程表”菜单中的&#x200B;**[!UICONTROL 提醒]**&#x200B;计数中自动移除。
