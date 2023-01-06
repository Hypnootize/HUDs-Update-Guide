# FIXING THE MVM MONEY

![Screenshot](https://raw.githubusercontent.com/Hypnootize/Huds-Update-Guide/master/Images/MvM_Money.png)

With the December 7 2022 patch the MvM money main parent `"CurrencyStatusPanel"` got moved from `Resource/UI/HudMannVsMachineStatus.res` to `Scripts/HudLayout.res`, without applying this fix the money will be missing or missplaced.

From your `Resource/UI/HudMannVsMachineStatus.res` copy the `"CurrencyStatusPanel"` element

```
"CurrencyStatusPanel"
{
		"ControlName"		"CCurrencyStatusPanel"
		"fieldName"			"CurrencyStatusPanel"
		"xpos"				"0"
		"ypos"				"r100"
		"wide"				"100"
		"tall"				"100"
		"xpos_minmode"		"65"
		"ypos_minmode"		"r88"
		"visible" 			"0"
		"enabled" 			"1"
		
		"PaintBackgroundType"	"2"
}
```

And then paste it inside `scripts/HudLayout.res`, it can be pasted at the end of the file right before the last bracket `}`
In case your HUD didn't feature the `Resource/UI/HudMannVsMachineStatus.res` at all you, still want to add the element to your `HudLayout.res` and in this case you can use the default element posted above.