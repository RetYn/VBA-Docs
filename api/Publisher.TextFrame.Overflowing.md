---
title: TextFrame.Overflowing property (Publisher)
keywords: vbapb10.chm3866649
f1_keywords:
- vbapb10.chm3866649
ms.prod: publisher
api_name:
- Publisher.TextFrame.Overflowing
ms.assetid: 5a0f053b-519a-1637-0d73-992c56cdd7f0
ms.date: 06/15/2019
ms.localizationpriority: medium
---


# TextFrame.Overflowing property (Publisher)

Indicates whether the text frame contains more text than can fit into the text frame. Read-only.


## Syntax

_expression_.**Overflowing**

_expression_ A variable that represents a **[TextFrame](Publisher.TextFrame.md)** object.


## Return value

MsoTriState


## Remarks

The **Overflowing** property value can be one of the **[MsoTriState](office.msotristate.md)** constants declared in the Microsoft Office type library.

## Example

This example increases the height of the selected text frame if it contains overflowing text.

```vb
Sub IncreaseTextBoxHeight() 
 With Selection.ShapeRange.TextFrame 
 If .Overflowing = msoTrue Then 
 Do 
 .Parent.Height = .Parent.Height + 36 
 Loop Until .Overflowing = msoFalse 
 End If 
 End With 
End Sub
```

[!include[Support and feedback](~/includes/feedback-boilerplate.md)]