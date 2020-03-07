# ADDING NEW WEAPONS METERS AND COUNTERS

With the new updates some new meters and kill counters got added to the game specifically:

```
HudItemEffectMeter_Cleaver.res
HudItemEffectMeter_Heavy.res
HudItemEffectMeter_Pyro.res
HudItemEffectMeter_Sapper.res
HudItemEffectMeter_SniperFocus.res
HudRocketPack.res

HudItemEffectMeter_Organs.res
```
Depending on how old the hud is you might have some of these already!

I have my own method to do this where I make the new meters work with the #base system so I have pretty much nothing to do.
Lets take as example HudItemEffectMeter_Pyro.res which is the new item meter for the phlogistinator.

What I would do is create a copy of HudItemEffectMeter.res but name the file HudItemEffectMeter_Pyro.res in this case and inside it I would delete everything and instead add a new code:

```
#base "HudItemEffectMeter.res"

"Resource/UI/HudItemEffectMeter_Pyro.res"
{
	HudItemEffectMeter
	{
		"ypos" "r120"
	}
}
```

What this does is making the files use the HudItemEffectMeter.res as a base on where to take the code from as you can see from the first line.
Then also adds a "ypos" specifically for HudItemEffectMeter_Pyro.res so we can make sure it doesn't overlap any other item meter by moving it to a different ypos than the HudItemEffectMeter.res

This method will work for any of the meters listed above, but note that for **HudItemEffectMeter_Organs.res** we wanna use **HudItemEffectMeter_Demoman.res** as a #base file since it acts like a heads counter!