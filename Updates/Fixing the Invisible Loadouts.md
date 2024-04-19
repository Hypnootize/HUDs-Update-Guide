# FIXING THE INVISIBLE LOADOUTS

![Screenshot](https://raw.githubusercontent.com/Hypnootize/Huds-Update-Guide/master/Images/Loadouts_Invisible.jpg)

With the April 19 2024 update, which introduced 64Bit for TF2, some menus such as loadout, backpack and more will fail to display correctly if the value for `"settitlebarvisible"` inside `Resource/UI/CharInfoPanel.res` is set to `"0"`, effectively making them invisible.

By default this value should be set to `"1"`, so this problem shouldn't apply to most HUDs but it might still be present for any HUD that mistakenly set the value to `"0"` in the past.

Note: after bringing back the value to `"1"`, depending on who the HUD is setup, it might also be needed to adjust the `"yoffset"` value, under the `"Sheet"` element, in order to ensure that the navigation bar is at the intended height.