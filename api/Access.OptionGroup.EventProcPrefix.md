---
title: OptionGroup.EventProcPrefix property (Access)
keywords: vbaac10.chm10819
f1_keywords:
- vbaac10.chm10819
ms.prod: access
api_name:
- Access.OptionGroup.EventProcPrefix
ms.assetid: a1a47d5b-5ba9-5071-bdc5-a5ea13d8d78a
ms.date: 02/21/2019
ms.localizationpriority: medium
---


# OptionGroup.EventProcPrefix property (Access)

Gets or sets the prefix portion of an event procedure name. Read/write **String**.


## Syntax

_expression_.**EventProcPrefix**

_expression_ A variable that represents an **[OptionGroup](Access.OptionGroup.md)** object.


## Remarks

For example, if you have a command button with an event procedure named **Details_Click**, the **EventProcPrefix** property returns the string **Details**.

Microsoft Access adds the prefix portion of an event procedure name to the event name with an underscore character ( _ ).




[!include[Support and feedback](~/includes/feedback-boilerplate.md)]