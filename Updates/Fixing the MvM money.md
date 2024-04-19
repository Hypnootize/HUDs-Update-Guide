# FIXING THE MVM MONEY

![Screenshot](https://raw.githubusercontent.com/Hypnootize/Huds-Update-Guide/master/Images/MvM_Money.png)

With the December 7 2022 patch the MvM money main parent `"CurrencyStatusPanel"` got moved from `Resource/UI/HudMannVsMachineStatus.res` to `Scripts/HudLayout.res`, without applying this fix the money will be missing or missplaced.

From your `Resource/UI/HudMannVsMachineStatus.res` copy the `"CurrencyStatusPanel"` element, here is how it looks on the default TF2 HUD:

```
"CurrencyStatusPanel"
{
	"ControlName"			"CCurrencyStatusPanel"
	"fieldName"			"CurrencyStatusPanel"
	"xpos"				"0"
	"ypos"				"r100"
	"wide"				"100"
	"tall"				"100"
	"xpos_minmode"			"65"
	"ypos_minmode"			"r88"
	"visible" 			"0"
	"enabled" 			"1"
		
	"PaintBackgroundType"		"2"
}
```

once copied, navigate to `scripts/HudLayout.res` and simply paste the element at the end of the file right **before** the last bracket `}`

In case your HUD didn't feature the `Resource/UI/HudMannVsMachineStatus.res` file at all, you can grab the default element from the TF2 default HUD `(posted above)` and follow the same process!

&nbsp;

*NOTE:* depending on the HUD the `Scripts/HudLayout.res` might be set up in different ways, some HUDs tend to split the hudlayout in multiple files, you can usually open the `HudLayout.res` and check if it features any `#base` links and from there pick the most appropriate file to paste the `"CurrencyStatusPanel"` in.
