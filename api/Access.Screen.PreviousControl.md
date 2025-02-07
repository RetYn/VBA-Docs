---
title: Screen.PreviousControl property (Access)
keywords: vbaac10.chm12489
f1_keywords:
- vbaac10.chm12489
ms.prod: access
api_name:
- Access.Screen.PreviousControl
ms.assetid: 089a62f7-2f3f-93e8-8e84-1b77d4f12e79
ms.date: 03/23/2019
ms.localizationpriority: medium
---


# Screen.PreviousControl property (Access)

Use the **PreviousControl** property together with the **Screen** object to return a reference to the control that last received the focus. Read-only.


## Syntax

_expression_.**PreviousControl**

_expression_ A variable that represents a **[Screen](Access.Screen.md)** object.


## Remarks

The **PreviousControl** property contains a reference to the control that last had the focus. After you establish a reference to the control, you can access all the properties and methods of the control.

You can't use the **PreviousControl** property until more than one control on any form has received the focus after a form is opened. Microsoft Access generates an error if you attempt to use this property when only one control on a form has received the focus.


## Example

The following example displays a message if the control that last received the focus wasn't the **txtFinalEntry** text box.

```vb
Public Function ProcessData() As Integer 
 
 ' No previous control error. 
 Const conNoPreviousControl = 2483 
 Dim ctlPrevious As Control 
 
 On Error GoTo Process_Err 
 
 Set ctlPrevious = Screen.PreviousControl 
 If ctlPrevious.Name = "txtFinalEntry" Then 
 ' 
 ' Process Data Here. 
 ' 
 ProcessData = True 
 Else 
 ' Set focus to txtFinalEntry and display message. 
 Me!txtFinalEntry.SetFocus 
 MsgBox "Please enter a value here." 
 ProcessData = False 
 End If 
 
Process_Exit: 
 Set ctlPrevious = Nothing 
 Exit Function 
 
Process_Err: 
 If Err = conNoPreviousControl Then 
 Me!txtFinalEntry.SetFocus 
 MsgBox "Please enter a value to process.", vbInformation 
 ProcessData = False 
 End If 
 Resume Process_Exit 
 
End Function
```




[!include[Support and feedback](~/includes/feedback-boilerplate.md)]