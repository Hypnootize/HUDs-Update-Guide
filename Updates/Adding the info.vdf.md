# ADDING THE INFO.VDF

*Every custom TF2 HUD needs the info.vdf file to be able to work, without it TF2 will always use the Default HUD as fallback even if there is a custom HUD inside the tf/custom folder.*

The info.vdf can be downloaded from the [Default HUD Files](https://github.com/Hypnootize/TF2-Default-Hud/archive/master.zip) and added to any custom HUD.
Once downloaded we want to put the file inside the HUD folder, sitting alongside the Resources and Scripts folders.

If your HUD already featured the info.vdf but the HUD doesn't work make sure the `ui_version` is set to the current supported vaule: `3`

```

"hud"
{
	"ui_version"	"3"
}

```