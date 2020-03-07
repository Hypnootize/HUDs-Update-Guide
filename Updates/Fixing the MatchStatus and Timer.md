# FIXING THE MATCHSTATUS AND TIMER

![Screenshot](https://raw.githubusercontent.com/Hypnootize/Huds-Update-Guide/master/Images/MatchStatus.png)

First of all, we are gonna need a new file **HudMatchStatus.res** so let’s take it from the [DEFAULT HUD FILES](https://github.com/Hypnootize/TF2-Default-Hud/archive/master.zip) and add it to our hud!

Now on the hud we are updating there should be a file called **HudObjectiveStatus.res** *(if you don’t have it the timer is either meant to be the default one or is already updated)*
Let’s open it and copy the whole code in it like so:

![Screenshot](https://raw.githubusercontent.com/Hypnootize/Huds-Update-Guide/master/Images/Objective_Status_OLD.png)

Let's then open the HudMatchStatus.res we just added and look for **"ObjectiveStatusPanel"**. 
Now for the last step let's select and replaced the **"ObjectiveStatusPanel"** code with the previously copied one from **HudObjectiveStatus.res** like shown on the screen.

![Screenshot](https://raw.githubusercontent.com/Hypnootize/Huds-Update-Guide/master/Images/MatchStatus_Replaced.png)

# GETTING THE TIMER INTO POSITION

Next thing we are going to do is getting the timer in position for both Control Point and King of the Hill maps.
To do that we need to add the **"if_match"** definitions to our timer codes so that the timer can change position when *tf_use_match_hud* is enabled.

## Normal Timer

Starting from **HudMatchStatus.res > "ObjectiveStatusPanel"** lets make sure our timer has a high enough "zpos" to be visible and is not hidden under the match status background by adding a new **if_match** code:

```

if_match
{
	"zpos" "5"
}

```

Once we do that we can start to move it around and get in into the right position by adding some **"xpos"** and **"ypos"** values to our **if_match**, something like:

```

if_match
{
	"xpos" "10"
	"ypos" "10"
	"zpos" "5"
}

```

Oviously every hud is different so I can't help there but it shouldn't too hard to figure it out, play around with the xpos / ypos and hud_reloadscheme until the timer is in position!

In some cases the timer font might be too big or small and in order to fix that we can add a new **"if_match"** to **HudMatchStatus.res > "ObjectiveStatusPanel" > "TimePanelValue"** to change it.
If we are unsure on which custom font can be used we can always go back to the default hud font: **"HudFontSmall"**


```

if_match
{
	"font" "HudFontSmall"
}

```

The final result should be something like that:

![Screenshot](https://raw.githubusercontent.com/Hypnootize/Huds-Update-Guide/master/Images/MatchStatus_IfMatch.png)

## King Of The Hill Timer


In order to fix the King of the Hill timers we need to work with **HudObjectiveKothTimePanel.res**

Again first thing let's increase the **"zpos"** by adding this new code at the start of the file

```

"HudKothTimeStatus"
{
	if_match
	{
		"zpos"		"5"
	}
}

```

Once thats done we can dedicate ourself to fix the positioning and fonts of the **"BlueTimer"** and **"RedTimer"** by adding new **if_match** definitions like we did before!

## Setup, Server Time Limit Etc...

One optional step will be fixing the "WaitingForPlayersLabel", "OvertimeLabel", "SuddenDeathLabel", "SetupLabel" and "ServerTimeLimitLabel" inside the **HudObjectiveTimePanel.res**