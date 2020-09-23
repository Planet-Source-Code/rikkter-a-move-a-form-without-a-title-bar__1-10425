<div align="center">

## A\*   Move a form without a title bar\!


</div>

### Description

Move any form without a title bar! You can use a label, command button, picturebox, anything to move the form.
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[rikkter](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/rikkter.md)
**Level**          |Beginner
**User Rating**    |4.7 (90 globes from 19 users)
**Compatibility**  |VB 5\.0, VB 6\.0
**Category**       |[Custom Controls/ Forms/  Menus](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/custom-controls-forms-menus__1-4.md)
**World**          |[Visual Basic](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/visual-basic.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/rikkter-a-move-a-form-without-a-title-bar__1-10425/archive/master.zip)





### Source Code

```
'Put this in a module:
Declare Sub ReleaseCapture Lib "user32" ()
Declare Function SendMessage Lib "user32" Alias "SendMessageA" (ByVal hWnd As Long, ByVal wMsg As Long, ByVal wparam As Integer, ByVal iparam As Long) As Long
Public Sub formdrag(theform As Form)
  ReleaseCapture
  Call SendMessage(theform.hWnd, &HA1, 2, 0&)
End Sub
'**************
'put this in the object that u want to move the form in the MouseDown:
formdrag Me
'thats it...vote for me if u like it...or email me if u need help...it should work...worked for me
```

