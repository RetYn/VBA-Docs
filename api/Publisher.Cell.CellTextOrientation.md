---
title: Cell.CellTextOrientation property (Publisher)
keywords: vbapb10.chm5111845
f1_keywords:
- vbapb10.chm5111845
ms.prod: publisher
api_name:
- Publisher.Cell.CellTextOrientation
ms.assetid: ad2c2f15-358c-7bbc-b249-b886a99ea4a5
ms.date: 06/06/2019
ms.localizationpriority: medium
---


# Cell.CellTextOrientation property (Publisher)

Returns or sets a **[PbTextOrientation](Publisher.PbTextOrientation.md)** constant that represents the flow of text in a specified table cell. Read/write.


## Syntax

_expression_.**CellTextOrientation**

_expression_ A variable that represents a **[Cell](Publisher.Cell.md)** object.


## Return value

PbTextOrientation


## Remarks

The **CellTextOrientation** property value can be one of the **PbTextOrientation** constants declared in the Microsoft Publisher type library.


## Example

This example increases the height of the cells in the first row, and then adds vertically-oriented heading text.

```vb
Sub VerticalText() 
 Dim rowTable As Row 
 Dim celTable As Cell 
 
 With ActiveDocument.Pages(2).Shapes(1).Table.Rows(1) 
 .Height = Application.InchesToPoints(1.5) 
 For Each celTable In .Cells 
 With celTable 
 .CellTextOrientation _ 
 = pbTextOrientationVerticalEastAsia 
 .TextRange.ParagraphFormat.Alignment _ 
 = pbParagraphAlignmentCenter 
 .TextRange.Text = "Column Heading " _ 
 & celTable.Column 
 End With 
 Next 
 End With 
End Sub
```

[!include[Support and feedback](~/includes/feedback-boilerplate.md)]