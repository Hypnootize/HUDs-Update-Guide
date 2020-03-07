# FIXING THE SCOREBOARD

## Fixing the scores section

The scoreboard file is located in **resource/ui/Scoreboard.res**

In order to fix the scoreboard we need to updated the **"scores"** sections values! (the part of the scoreboard that displays the avatar – name – score – class – ping etc… of every player)

Basically we can replace everything after "tabposition" "0" with these values that I found to work the best for most of the huds:

```
"tabPosition"				"0"
"medal_width"				"12"
"avatar_width"				"55"
"spacer"					"2"
"name_width"				"85"
"nemesis_width"				"15"
"class_width"				"15"
"score_width"				"20"
"ping_width"				"20"
"killstreak_width"			"12"
"killstreak_image_width"	"12"
```

These values are the most generic values I could find and they work perfectly with most of the huds.
But there might be cases where the ping or any other value is getting cut off, so all you need to do is increase that value until you can see it entirely!

## Preventing the stats from turning white

This is a completly optional thing but I'm covering it as a lot of people asked me about this!
Some user don't like the fact that their stats turn green when active so to prevent it and keep the intended color from the hud we can edit the "fieldname" of each stat entry.
If we scroll down and look for **"LocalPlayerStatsPanel"** we should be able to find each stat entry and to prevent them from turning green we can just add a letter at the end of their "fieldname".
Lets take as example the kills we will need to edit the "fieldname" of "Kills" to "Kills1". And then do the same for:

```
"Kills"
"Deaths"
"Assists"
"Captures"
"Destruction"
"Defenses"
"Domination"
"Revenge"
"Invuln"
"Headshots"
"Teleports"
"Healing"
"Backstabs"
"Bonus"
"Support"
"Damage"
```


