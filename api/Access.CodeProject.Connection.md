---
title: CodeProject.Connection property (Access)
keywords: vbaac10.chm12720
f1_keywords:
- vbaac10.chm12720
ms.prod: access
api_name:
- Access.CodeProject.Connection
ms.assetid: 3fb6bb6f-83c9-f682-79fc-6cdace654d26
ms.date: 02/27/2019
ms.localizationpriority: medium
---


# CodeProject.Connection property (Access)

Use the **Connection** property to return a reference to the current ActiveX Data Objects (ADO) **Connection** object and its related properties. Read-only **Connection**.


## Syntax

_expression_.**Connection**

_expression_ A variable that represents a **[CodeProject](Access.CodeProject.md)** object.


## Remarks

Use the **Connection** property to refer to the **Connection** object of the Access project or Access database code database object. Use the **Connection** property to call methods on the **Connection** object such as **BeginTrans** and **CommitTrans**.

> [!NOTE] 
> The **Connection** property actually returns a reference to a copy of the ActiveX Data Object (ADO) connection for the active database. Thus, applying the **Close** method or in anyway attempting to alter the connection through the **Connection** object's methods or properties will have no affect on the actual connection object used by Microsoft Access to hold a live connection to the current database. Because the **Connection** property is the main Shape provider connection, the following information is necessary when using this property.




[!include[Support and feedback](~/includes/feedback-boilerplate.md)]