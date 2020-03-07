# ADDING THE INFO.VDF

*The info.vdf file is what makes the hud load when you launch TF2, without it the game will always use the Default Hud even if there is a custom hud inside the tf/custom folder.*

First thing lets take the Info.vdf file from the [Default Hud Files](https://github.com/Hypnootize/TF2-Default-Hud/archive/master.zip) and add it to our hud, it goes in the main hud folder (see note)

Next step lets open the info.vdf file and change the name of it to match the name of the hud folder.
For example, if the main folder of the hud is named **Hypnotize Hud** I will edit it to look like this:

```

"hypnotize hud"
{
	"ui_version"	"3"
}

```

*note: for main folder is intended the folder which contains the resource & scripts folders inside*