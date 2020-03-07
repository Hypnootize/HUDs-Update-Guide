# UPDATING THE ANIMATIONS

*The animations are used to animate a lot of hud parts such as health buffs, ready ubercharges, main menu's moving parts and many more.*
*Having the animations file outdated could be some sort of a risk since old animations or missing animations in some cases could even crash your game.*
*Luckily for us there is now a method to make sure the animations auto-update.*

The first thing we need to do is go to our scripts folder and create a new .txt file named HudAnimations_Manifest.txt
Inside it we will add the paths to the animations files which can be found here 

```

hudanimations_manifest
{
	"file" "scripts/hudanimations.txt"
	"file" "scripts/hudanimations_custom.txt"
	"file" "scripts/hudanimations_tf.txt"
}

```

lets copy the whole thing and paste it to our HudAnimations_Manifest.txt

Inside the scripts folder we should now have 2 animations files

* HudAnimations_Manifest.txt
* HudAnimations_tf.txt

The next step is renaming the HudAnimation_tf to > HudAnimations_Custom just so it matches what we just added inside the HudAnimations_Manifest.

Now the last thing we need to do is removing all the unneeded codes inside the HudAnimations_Custom.

We can pretty much delete everything BUT these sections:

* Health Bonus Pulse
* Health Dying Pulse
* HudLowAmmoPulse
* HudMedicCharged
* And the HudTournamentSetupPanelOpen/Close if it’s different from the default hud

If you have doubts on what you can delete and what not you can compare your hud animations with the default hud ones, you want to delete every code that looks exactly the same as the default one.