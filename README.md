<div align="center">

## No Refresh, No Backspace, No Right Click


</div>

### Description

To disable the RIGHT CLICK, the BACKSPACE (for navigation purposes), and the REFRESH.
 
### More Info
 
Please note that for this script to run effectively it is recommended that you open a new browser using script to disable the navigation, link bars, etc., etc. Also, the cool thing about this code is that the JavaScript disables itself once the cursor is in a text are box, or input box - VERY COOL!

No Right Click, No Refresh, No Backspace, and other methods to refresh or navigate back in a browser. IE v5.0 + ONLY



----

PLEASE NOTE THAT PLANET SOURCE CODE LIKES TO TRANSFORM THE CASE OF SOME PARTS OF CODE THAT IS SUBMITTED. MAKE SURE ALL OF THIS JAVASCRIPT IS LOWERCASE!

----




<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Matt Khoury](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/matt-khoury.md)
**Level**          |Advanced
**User Rating**    |4.0 (20 globes from 5 users)
**Compatibility**  |HTML
**Category**       |[Internet/ Browsers/ HTML](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/internet-browsers-html__4-9.md)
**World**          |[ASP / VbScript](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/asp-vbscript.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/matt-khoury-no-refresh-no-backspace-no-right-click__4-6721/archive/master.zip)

### API Declarations

Created By: Matthew J. Khoury, Copyright 2001 [Please list my name where you use this code.]


### Source Code

```
<HTML>
<HEAD>
	<TITLE>NO REFRESH, NO REFRESH, NO BACKSPACE, NO ALT-BACKSPACE, ETC., ETC..</TITLE>
<SCRIPT LANGUAGE=JAVASCRIPT>
var oLastBtn=0;
	bIsMenu = false;
	//No RIGHT CLICK************************
	// ****************************
	if (window.Event)
	document.captureEvents(Event.MOUSEUP);
	function nocontextmenu()
	{
	event.cancelBubble = true
	event.returnValue = false;
	return false;
	}
	function norightclick(e)
	{
	if (window.Event)
	{
	if (e.which !=1)
	return false;
	}
	else
	if (event.button !=1)
	{
	event.cancelBubble = true
	event.returnValue = false;
	return false;
	}
	}
	document.oncontextmenu = nocontextmenu;
	document.onmousedown = norightclick;
	//**************************************
	// ****************************
	// Block backspace onKeyDown************
	// ***************************
	 function onKeyDown() {
	 	if ( (event.altKey) || ((event.keyCode == 8) &&
	 			(event.srcElement.type != "text" &&
	 			event.srcElement.type != "textarea" &&
	 			event.srcElement.type != "password")) ||
	 			((event.ctrlKey) && ((event.keyCode == 78) || (event.keyCode == 82)) ) ||
	 			(event.keyCode == 116) ) {
	 		event.keyCode = 0;
	 		event.returnValue = false;
	 	}
	 }
</SCRIPT>
</HEAD>
<BODY onKeyDown="onKeyDown();" BGCOLOR="#639ace" MARGINHEIGHT="0" MARGINWIDTH="0" TOPMARGIN="0" LEFTMARGIN="0">
<TABLE WIDTH="100%" BORDER="0" CELLSPACING="0" CELLPADDING="0">
	<TR>
		<TD><H3>NO REFRESH, NO REFRESH, NO BACKSPACE, NO ALT-BACKSPACE, ETC., ETC..</H3></TD>
	</TR>
	<TR>
		<TD>Please note that for this script to run effectively it is recommended that you open a new browser using script to disable the navigation, link bars, etc., etc..</TD>
	</TR>
</TABLE>
</BODY>
</HTML>
```

