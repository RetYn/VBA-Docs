---
title: GetText method (Microsoft Forms)
keywords: fm20.chm2012320
f1_keywords:
- fm20.chm2012320
ms.prod: office
ms.assetid: 7d714405-4d3e-23e3-cedb-8a6a7fd07269
ms.date: 11/15/2018
ms.localizationpriority: medium
---


# GetText method (Microsoft Forms)

Retrieves a text string from the **[DataObject](dataobject-object.md)** using the specified format.

## Syntax

_String_ = _object_. **GetText(** [ _format_ ] **)**

The **GetText** method syntax has these parts:

|Part|Description|
|:-----|:-----|
| _object_|Required. A valid object name.|
| _format_|Optional. A string or integer specifying the format of the data to retrieve from the **DataObject**.|

## Settings

The settings for _format_ are:

|Value|Description|
|:-----|:-----|
|1|Text format.|
|A string or any integer other than 1|A user-defined **DataObject** format passed to the **DataObject** from **SetText**.|

## Remarks

The **DataObject** supports multiple formats, but only supports one data item of each format. For example, the **DataObject** might include one text item and one item in a custom format; but cannot include two text items.
If no format is specified, the **GetText** method requests information in the Text format from the **DataObject**.

## See also

- [GetFormat method](./getformat-method.md)
- [Microsoft Forms examples](examples-microsoft-forms.md)
- [Microsoft Forms reference](reference-microsoft-forms.md)
- [Microsoft Forms concepts](concepts-microsoft-forms.md)

[!include[Support and feedback](~/includes/feedback-boilerplate.md)]