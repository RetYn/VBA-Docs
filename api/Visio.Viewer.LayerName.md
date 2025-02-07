---
title: Viewer.LayerName property (Visio Viewer)
ms.prod: visio
api_name:
- Visio.Viewer.LayerName
ms.assetid: ebf2b8da-7c4d-b67c-9f8c-17629f1d8214
ms.date: 06/21/2019
ms.localizationpriority: medium
---


# Viewer.LayerName property (Visio Viewer)

Gets the name of the layer at the specified index in the drawing open in Microsoft Visio Viewer. Read-only.


## Syntax

_expression_.**LayerName** (_LayerIndex_)

_expression_ An expression that returns a **[Viewer](Visio.Viewer.md)** object.


## Parameters

|Name|Required/Optional|Data type|Description|
|:-----|:-----|:-----|:-----|
|_LayerIndex_|Required| **Long**|The index of the layer in the collection of layers in the drawing open in Visio Viewer.|

## Return value

**String**


## Remarks

The collection of layers is one-based, so the index of the first layer in the collection is 1. If there are no layers in the drawing, or if there is no layer at index position _LayerIndex_, the **LayerName** property returns nothing.


## Example

The following code gets the name of all the layers in the drawing open in Visio Viewer.

```vb
Dim intCounter As Integer

For intCounter = 1 To vsoViewer.LayerCount

    Debug.Print vsoViewer.LayerName(intCounter)

Next intCounter
```

[!include[Support and feedback](~/includes/feedback-boilerplate.md)]