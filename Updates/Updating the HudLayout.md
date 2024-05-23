# UPDATING THE HUDLAYOUT

The first thing we need to do is lauch TF2 and open the console to look for errors.
What we are looking for are the errors that say "Hud element" ...' "doesn't have an entry" ... "in scripts/HudLayout.res"

![Screenshot](https://raw.githubusercontent.com/Hypnootize/Huds-Update-Guide/master/Images/HudLayout_Errors.png)

Let’s take as example the first error line. It says that the "MatchSummary" entry is missing in our HudLayout.

What we need to do is:

1. Open the [Default Hud](https://github.com/Hypnootize/TF2-Default-Hud/archive/master.zip) Scripts/HudLayout.res
2. Search for "MatchSummary"
3. Copy the whole code and paste it to our HudLayout
4. Pasting it the end of the file is fine, but be sure to respect the brackets

![Screenshot](https://raw.githubusercontent.com/Hypnootize/Huds-Update-Guide/master/Images/HudLayout_Fix.png)

Repeat the steps for each one of the errors the console displays.

**Special Case Changes (Optional):**

In the spirit of keeping the HUD layout file clean, some entries that have been removed or renamed can be updated as such:

 - `CTFKillStreakNotice` should be renamed to `CTFStreakNotice`
 - `HudDamageIndicator` should be modified to be an empty entry
 - `MatchMakingContainer` should be removed
