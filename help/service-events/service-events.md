---
product: campaign
solution: Campaign
title: 识别关键联系人和事件
description: 了解如何在 Adobe 中识别实例中发生的事件和关键联系人。
feature: Control Panel
role: Architect
level: Intermediate
exl-id: d230aae6-4f0e-4201-bb3c-0e3f83a7c1b8
source-git-commit: 5e2a5975a4a2ced4b23a18900309fc537daf13c0
workflow-type: tm+mt
source-wordcount: '749'
ht-degree: 43%

---

# 识别关键联系人和事件 {#keycontacts-events}

>[!CONTEXTUALHELP]
>id="cp_servicecalendar_serviceevents"
>title="服务日历"
>abstract="“关键联系人”部分列出了可联系的 Adobe 人员，以便您针对实例提出任何请求或问题。 在服务事件日历部分中，您可以识别选定实例的过去/即将发行的版本和警报，以及设置给定事件的提醒。"

>[!IMPORTANT]
>
>服务日历将在测试版中提供，如有频繁更新和修改，恕不另行通知。

要有效监控Campaign实例，必须跟踪可能影响实例的重要事件。 利用控制面板，可识别新版本、升级、修补程序、热修复程序等事件。 并提供任何请求或问题的关键Adobe联系人列表。

此信息可从 **[!UICONTROL Service Calendar]** 卡片。

## 关键联系人 {#key-contacts}

**[!UICONTROL Key contacts]** 部分列出了可联系的 Adobe 人员列表，以便您针对实例提出任何请求或问题。

>[!NOTE]
>
>此部分仅显示托管服务帐户的信息。

![](assets/service-events-contacts.png)

主要联系人包括以下角色：

* **[!UICONTROL TAM]**：技术客户经理、
* **[!UICONTROL CSM]**：客户成功经理、
* **[!UICONTROL Deliverability]**：可交付性操作联系人、
* **[!UICONTROL Transition Manager]**：Managed Services 过渡经理（仅限 Managed Services 帐户）、
* **[!UICONTROL On-boarding Specialist]**：分配给帐户的专家，可帮助您熟悉 Campaign Classic（仅限 Managed Services 帐户）。

## 跟踪重要事件 {#events}

的 **[!UICONTROL Service Event Calendar]** 部分显示所有过去和即将发布的版本，以及用户在控制面板电子邮件警报中订阅的警报。 此外，控制面板还允许用户为所选实例设置提醒和标记相关事件，以使其更好地组织和高效。

事件显示在日历或列表中。 您可以使用 **[!UICONTROL Calendar]** 和 **[!UICONTROL List]** 按钮。

![](assets/service-events-calendar.png)

<table><tr style="border: 0;">
<td><img src="assets/do-not-localize/nav-buttons.png">
</td><td>在日历视图中，右上角提供导航按钮，帮助您浏览各个事件。 使用 <b>双箭头</b> 导航到选定月份之后/之前出现的第一个事件，以及 <b>单箭头</b> 从一个月导航到另一个月。 单击 <b>圆圈按钮</b> 回到今天的观点。</td>
</tr></table>

显示三种类型的事件：

* **提醒** 由用户设置，以便在事件发生之前收到通知。 日历视图中这些图标以绿色显示。 [了解如何设置提醒](#reminders)
* **警报** 控制面板通过电子邮件发送，以通知用户其实例中存在的问题，如存储过载或SSL证书过期。 在日历视图中，这些图标以橙色显示。 事件描述根据登录用户对电子邮件警报的订阅，指定是否将警报发送给登录用户。 [进一步了解控制面板电子邮件警报功能](../performance-monitoring/using/email-alerting.md)

* **版本** 指示实例的过去部署和即将进行的部署，在日历视图中分别以灰色和蓝色显示。 事件详细信息指定与每个部署关联的版本类型：

   * **[!UICONTROL General availability]**：最新发布的稳定版本。
   * **[!UICONTROL Limited availability]**：仅限按需部署。
   * **[!UICONTROL Release candidate]**：工程部门已验证。 等待生产校样。
   * **[!UICONTROL Pre release]**：提前提供以满足特定客户需求。
   * **[!UICONTROL No longer available]**：该版本不存在重大问题，但新版本可供使用，并包含其他错误修复。 需要进行升级。
   * **[!UICONTROL Deprecated]**：版本嵌入已知回归。
不再支持该版本。 必须进行升级。

可为一个或多个即将发生的事件分配一个标记以进行跟踪。 要实现此目的，请单击事件名称旁边的省略号按钮。

![](assets/service-events-flag.png)

## 设置提醒 {#reminders}

使用“服务日历”，您可以设置提醒，以便在事件发生之前通过电子邮件接收通知。

>[!NOTE]
>
>要接收有关即将发生的事件的通知，请确保您已在控制面板中订阅电子邮件警报。[了解详情](../performance-monitoring/using/email-alerting.md)

要针对某一事件设置警报，请执行以下步骤：

1. 将鼠标悬停在要提醒的事件上，或单击列表视图中的椭圆按钮并选择 **[!UICONTROL Set Reminder]**.

1. 为提醒提供一个标题，并选择要在事件发生之前收到通知的日期。

   ![](assets/service-events-set-reminder.png)

   >[!NOTE]
   >
   >如果您未订阅控制面板警报，则会显示一条消息，您可以进行注册以接收电子邮件通知。

1. 现已为选定事件设置提醒。您可以随时将鼠标悬停在该事件上以显示其标题。

   ![](assets/service-events-reminder.png)

   >[!NOTE]
   >
   >您最多可以为同一事件设置 2 个提醒。

1. 在提醒中指定的日期，会发送一封电子邮件，通知您即将发生的事件，并将提醒从“Service Calendar”菜单中的 **[!UICONTROL Reminders]** 计数中自动删除。
