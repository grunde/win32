---
Description: Instructs an IME window to retrieve the logical font used for displaying intermediate characters in the composition window. To send this command, the application uses the WM\_IME\_CONTROL message with the parameter settings shown below.
ms.assetid: 43db70b6-f8bc-4241-9096-5d91fd1e332b
title: IMC\_GETCOMPOSITIONFONT command
ms.technology: desktop
ms.prod: windows
ms.author: windowssdkdev
ms.topic: article
ms.date: 05/31/2018
---

# IMC\_GETCOMPOSITIONFONT command

Instructs an IME window to retrieve the logical font used for displaying intermediate characters in the composition window. To send this command, the application uses the [**WM\_IME\_CONTROL**](wm-ime-control.md) message with the parameter settings shown below.


```C++
LRESULT IMC_GETCOMPOSITIONFONT
```



## Parameters

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

Set to IMC\_GETCOMPOSITIONFONT.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Pointer to a [**LOGFONT**](https://msdn.microsoft.com/windows/desktop/57658a03-0a6d-4a28-a7c1-c65ec145beb4) structure that receives information about the logical font.

</dd> </dl>

## Return Value

Returns 0 if successful, or a nonzero value otherwise.

## Requirements



|                                     |                                                                                                      |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows 2000 Professional \[desktop apps only\]<br/>                                           |
| Minimum supported server<br/> | Windows 2000 Server \[desktop apps only\]<br/>                                                 |
| Header<br/>                   | <dl> <dt>Imm.h (include Windows.h)</dt> </dl> |



## See also

<dl> <dt>

[Input Method Manager](input-method-manager.md)
</dt> <dt>

[Input Method Manager Commands](input-method-manager-commands.md)
</dt> </dl>

 

 



