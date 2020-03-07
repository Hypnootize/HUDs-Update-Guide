# FIXING THE TOURNAMENT PANEL

![Screenshot](https://raw.githubusercontent.com/Hypnootize/Huds-Update-Guide/master/Images/Tournament_Panel.jpg)

We are looking at **resource > ui > HudTournament.res**

I have my own way of doing this which might not be the best or easiest but is the best way I found that works with every hud out there.

## Making the tournament panel cover the whole screen

I really like to have my Tournament Panel cover the entire screen so I won't be bothered with elements getting cut later on, and to do that we will set the first "xpos", "ypos", "wide", "tall" we find in the file to be like that:

```
"xpos" "0"
"ypos" "0"
"wide" "f0"
"tall" "f0"
```

**If your values were already like above skip the centering step**

## Centering the tournament panel

Now since we edited the "xpos" of the whole panel our Tournament Ready Panel is not gonna be cenetered anymore and in order to bring it back to the center of the screen we need to edit these elements "xpos":

```
"HudTournamentBG"
"TournamentLabel"
"HudTournamentBLUEBG"
"TournamentBLUELabel"
"TournamentBLUEStateLabel"
"HudTournamentREDBG"
"TournamentREDLabel"
"TournamentREDStateLabel"
"TournamentConditionLabel"
"HudTournamentBGHelp"
"TournamentInstructionsLabel"
"TournamentInstructionsLabelShadow"
"TournamentReadyHintIcon"
```

You might be missing some of these or you might have some not listed but the general rule is to edit the xpos of the elemets starting from "HudTournamentBG" until we reach "CountdownBG" *(excluded)*
Anyway lets fix them, before we changed the values from "c-125" to "0" now we need to do the opposite!
If "HudTournamentBG" "xpos" is "0" we need to change it to "c-125" for example, or if it is "50" it will now be "c-75" or again if it is "150" it will now be "c25" you see where I'm going!

## Making the tournament panel disappear for MvM and ReadyUp modes

Now that our Tournament Panel is back in position let's make it disappear when we are in a mvm game or self ready mode game by adding the **if_mvm / if_competitive / if_readymode** alteratives.

```
if_mvm
{
	"visible"		"0"
}

if_competitive
{
	"visible"		"0"
}

if_readymode
{
	"visible"		"0"
}
```

In order to achieve something like this:

```
"TournamentLabel"
{	
	"ControlName"	"Label"
	"fieldName"		"TournamentLabel"
	"font"			"HudFontSmall"
	"xpos"			"5"
	"ypos"			"3"
	"zpos"			"1"
	"wide"			"240"
	"tall"			"19"
	"autoResize"	"0"
	"pinCorner"		"0"
	"visible"		"1"
	"enabled"		"1"
	"wrap"			"0"
	"labelText"		"%tournamentstatelabel%"
	"textAlignment"	"center"
	"proportionaltoparent"	"1"
	
	if_mvm
	{
		"visible"		"0"
	}

	if_competitive
	{
		"visible"		"0"
	}

	if_readymode
	{
		"visible"		"0"
	}
}
```

Usually we want to make everything disappear but keep the ReadyUp Instructions and Game Conditions that said we can apply these new values like shown above to this list of elemets:

```
"HudTournamentBG"
"TournamentLabel"
"HudTournamentBLUEBG"
"TournamentBLUELabel"
"TournamentBLUEStateLabel"
"HudTournamentREDBG"
"TournamentREDLabel"
"TournamentREDStateLabel"
"HudTournamentBGHelp"
```

## Fixing the class ReadyUP

![Screenshot](https://raw.githubusercontent.com/Hypnootize/Huds-Update-Guide/master/Images/Class_ReadyUP.jpg)

Now that the harder part is done we need to make sure that the Class ReadyUp Panels are showing up correctly.
At the start of our HudTournament.res file we should have this part of code:

```
"team1_player_base_offset_x"	"-75"
"team1_player_base_y"			"0"
"team1_player_delta_x"			"-47"
"team1_player_delta_y"			"0"
"team2_player_base_offset_x" 	"25"
"team2_player_base_y"			"0"
"team2_player_delta_x"			"47"
"team2_player_delta_y"			"0"
```

We need to add a new line to this for the competitive mode: **"teams_player_delta_x_comp"** and his value should be the same as **"team2_player_delta_x"** in this case we will set both to **"47"**

Now the very last setp, we need to decide where on the screen we want these Class ReadyUp Panels to show up so to do that we will need to add once again the **if_mvm / if_competitive / if_readymode** to the part of code shown above.


```
"team1_player_base_offset_x"	"-75"
"team1_player_base_y"			"0"
"team1_player_delta_x"			"-47"
"team1_player_delta_y"			"0"
"team2_player_base_offset_x" 	"25"
"team2_player_base_y"			"0"
"team2_player_delta_x"			"47"
"team2_player_delta_y"			"0"
"teams_player_delta_x_comp"		"47"

if_mvm
{
	"team1_player_base_y"		"80"
}
if_competitive
{
	"team1_player_base_y"		"60"
}
if_readymode
{
	"team1_player_base_y"		"60"
}
```

For example here the Class Panels are 60 pixel down from the top of the screen while mvm will be 80 pixel down. 0 will be on the very top of the screen!