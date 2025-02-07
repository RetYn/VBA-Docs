---
title: References.Item method (Access)
keywords: vbaac10.chm12640
f1_keywords:
- vbaac10.chm12640
ms.prod: access
api_name:
- Access.References.Item
ms.assetid: c159f3ff-b642-7151-c167-3699a6300f5f
ms.date: 03/23/2019
ms.localizationpriority: medium
---


# References.Item method (Access)

The **Item** method returns a specific member of a collection either by position or by key. **Reference** object.


## Syntax

_expression_.**Item** (_var_)

_expression_ A variable that represents a **[References](Access.References.md)** object.


## Parameters

|Name|Required/Optional|Data type|Description|
|:-----|:-----|:-----|:-----|
| _var_|Required|**Variant**|An expression that specifies the position of a member of the collection.<br/><br/>If a numeric expression, the _var_ argument must be a number from 1 to the value of the collection's **Count** property.<br/><br/>If a string expression, the _var_ argument must be the name of a member of the collection.|

## Return value

Reference


## Remarks

If the value provided for the _var_ argument doesn't match any existing member of the collection, an error occurs.

The **Item** method is the default member of the **References** collection, so you don't have to specify it explicitly. For example, the following two lines of code are equivalent.

```vb
Debug.Print References(1).Name
```

```vb
Debug.Print References.Item(1).Name
```



[!include[Support and feedback](~/includes/feedback-boilerplate.md)]