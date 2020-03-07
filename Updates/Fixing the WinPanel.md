# FIXING THE WINPANEL

![Screenshot](https://raw.githubusercontent.com/Hypnootize/Huds-Update-Guide/master/Images/Winpanel.jpg)

We can find it here: **resource/ui/Winpanel.res**

Right at the start of the file we should have two elements **"BlueScoreBG" "RedScoreBG"**.
What we need to do first is change both **name** and **"fieldName"** to **"BlueScoreBG2"** and **"RedScoreBG2"**

*If you didn’t have these 2 elemets don't worry just do what it follows!*

Then add two new codes called **"BlueScoreBG"** **"RedScoreBG"** and let’s make them invisibles by setting the "wide" "tall" "visible" and "enabled" values to "0" like shown:

```
"BlueScoreBG"
{
	"ControlName"	"EditablePanel"
	"fieldName"		"BlueScoreBG"
	"wide"			"0"
	"tall"			"0"
	"visible"		"0"
	"enabled"		"0"
}
"RedScoreBG"
{
	"ControlName"	"EditablePanel"
	"fieldName"		"RedScoreBG"
	"wide"			"0"
	"tall"			"0"
	"visible"		"0"
	"enabled"		"0"
}

"BlueScoreBG2"
{
	"ControlName"	"EditablePanel"
	"fieldName"		"BlueScoreBG2"
	"xpos"			"50"
	"ypos"			"15"
	"wide"			"135"
	"tall"			"40"
	"autoResize"	"0"
	"pinCorner"		"0"
	"visible"		"1"
	"enabled"		"1"
	"border"		"TFFatLineBorderBlueBGMoreOpaque"
}
"RedScoreBG2"
{
	"ControlName"	"EditablePanel"
	"fieldName"		"RedScoreBG2"
	"xpos"			"197"
	"ypos"			"15"
	"wide"			"135"
	"tall"			"40"
	"autoResize"	"0"
	"pinCorner"		"0"
	"visible"		"1"
	"enabled"		"1"
	"border"		"TFFatLineBorderRedBGMoreOpaque"
}
```

Last thing we need to do is add a new element.
Let's scroll down until we find the **"WinningTeamLabel"** and just above that we will add this new element:

```
"WinPanelBGBorder"
{
	"ControlName"	"EditablePanel"
	"fieldName"		"WinPanelBGBorder"
	"wide"			"0"
	"tall"			"0"
	"visible"		"0"
	"enabled"		"0"
}
```

The Winpanel should now be back and showing each time you win or lose a round!